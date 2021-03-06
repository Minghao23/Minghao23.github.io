---
layout: post
title: "《代码大全》笔记 - 基本数据类型和不常见的数据类型"
class: Technology
categories: ["Other"]
keywords: Code Complete basic type pointer
---

本文主要是对《代码大全第二版》中第 12 章和第 13 章的阅读总结，另外加一些从自己日常应用角度的理解。

> 代码大全2中文版pdf下载：链接：http://pan.baidu.com/s/1jHQ1tAm 密码：4zd9 **(侵删)**

## 基本数据类型

基本数据类型涵盖了其他所有数据类型和数据结构的最小构造块，对各种语言都有一定的通用性。作为程序员对其都有基本的了解，所以本文主要是从通用角度解释各种类型使用中的注意事项。也就是**应该怎么用**。

### 数值概论

基本类型的划分一般都包括数值类型，字符类型和逻辑类型，数值类型常常又包括各种精度的整型和浮点型。以下问题是在所有数值类型的额使用中都比较常见的。

**避免使用神秘数值**

比如看下面这个 python 代码片段

``` python
def next_motion(ball_handler, ...):
    if ball_handler == 95:
        run_to_weak_side()
    ...
```

这个 95 就是所谓的 Magic Number，乍一看完全不知道这段代码是什么意思，其实这是一段篮球机器人的代码，意思是如果持球人的号码是秋实，那么立刻转去弱侧接球。那么如果用具名常量来代替这个数，代码变为

``` python
def next_motion(ball_handler, ...):
    if ball_handler == QS_JERSEY_NUMBER:
        run_to_weak_side()
    ...
```

就很容易读懂代码的含义，增加了可读性。另外，如果秋实哪天一高兴换了号码，这段代码也不用动，即增加了代码的鲁棒性。

【建议】在实际使用中，我们建议所有除了 0 和 1 以外的数字都尽可能用具名常量来代替。0 和 1 可以用来代表索引初值，增量和减量。

**预防除零错误**

【一个习惯】每次在使用除法的时候都要考虑除零错误，如果有必要，则需要提前对一些 corner cases 做检查。

**避免混合类型的比较**

如果直接使用类型不同的两个数值去比较，编译器会把其中一种转化为另一种，执行一些四舍五入计算后才得出结果，这样你的程序还能不能跑起来就变成一个运气游戏了。

【建议】在可以预测到出现不同类型的数值比较之前先手动做类型转换

### 整数

**整数除法**

大部分语言中，两个整数相除的结果只会取整数部分（JS 不会）。所以如果我们一定要做整数除法的时候，请把除法放在其他操作的最后，尽可能的减少除到 0 所带来的影响，不过我觉得，正常的程序员都不会这么蠢。

```python
x = 7 / 10 * 10  # x = 0
x = 7 * 10 / 10  # x = 7
```

**整数溢出**

整数的取值范围由你使用的类型确定。比如 16-bit 无符号的整数，取值范围就是 0 至 65535，8-bit 有符号的整数，取值范围为 -128 至 127。看下面一段二分查找的 python 代码

```python
def binary_search(super_large_array, target):
    # assume that the array is sorted
    start = 0
    end = len(super_large_array)

    while start < end:
        mid = (start + end) / 2
        if super_large_array[mid] < target:
            start = mid + 1
        elif super_large_array[mid] > target:
            end = mid - 1
        else:
          return super_large_array[mid]
    return -1
```

因为这是一个超级大的数组，所以必定就要考虑数值溢出的问题。而往往最容易忽略的数值溢出都发生在计算的中间过程中，比如上述代码中计算 mid 的部分。其中 start + end 的上限是二倍的数组长度，如果数组的长度大于二分之一整数最大值，就有可能出现整数溢出。为了避免这个情况，我们改写 mid 的计算为 start + (start - end) / 2。

【建议】在真正开始写代码之前，考虑清楚程序未来的扩展情况，并选取合适的整数类型。

**与包装类型的区别**

在一些语言中，比如 Java，会提供一些包装好的类型来拓展基本类型的功能。那他们与基本类型有什么区别呢？看下面一段 Java 代码

```java
public void proofIntegerIsFoolish() {
    Integer a1 = 127;
    Integer b1 = 127;
    System.out.println(a1 == b1);

    Integer a2 = 128;
    Integer b2 = 128;
    System.out.println(a2 == b2);
}
```

你会发现程序第一行会输出 true， 而第二行会输出 false。为什么呢？首先要知道 Integer 是什么。Integer 是 Java 为 int 封装的一个包装类，int 则是基本的数据类型。是类在使用的时候就需要实例化，而变量名则是指向实例化后的对象的引用。而 int 直接储存数值，不需要实例化。我们知道在 Java 中双等号操作符比较的是两个引用是否指向同一个对象，那么两个 Integer 的引用必然是不相同的。而上述代码中的初始化方式 `Integer a = 127` 实际会翻译为 `Integer a = Integer.valueOf(127)`，我们查看 `valueOf()` 的代码可以发现，对 -128 到 127 之间的整数，Integer 会做一个缓存，当新的与缓存内的对象数值相同的 Integer 被创建时，直接返回缓存中的对象，如果大于 128，则 new 一个新的对象。

所以，不要使用 Integer。

### 浮点数

**避免数量级相差巨大的加减运算**

32 位的浮点变量，1,000,000.00 + 0.1 可能会得到 1,000,000.00，因为 32 位不能给你足够的有效位数包容他们之间的数值空间。这个问题看似影响不大，但是如果这个加法加了 1,000,000 次，那就有问题了。一些算法书上讲到，把任何连续加法的顺序都改为从最小的数开始顺序相加，可以最大可能的避免精度问题，但是很蠢。在金融相关机构中，这个问题尤为重要，大家都知道比特币现在大约 1 万美元一个，而很多其他货币交易时的手续费都是以 BTC 记录的，可能某一单的手续费是 0.0000001 BTC，那么在交易平台记账时就会遇到这个问题。其中一个解决方案是，使用整数来分割管理整数和小数部分，从而彻底避免浮点数带来的一系列问题，当然也需要耗费更多的计算资源。说个题外话，大家都知道比特币的总量是2100万，其实它就是考虑到了计算机浮点数的最大精度。一个比特币最多可以分割成1亿份，每一份叫做 1 “聪”。浮点表示法本质上就是二进制的科学记数法，它把一个小数储存为 a = m × b^e 的形式。在双精度浮点数中，总长为 16 位。符号位数为 1，指数位数为 11，尾数位数为 52。这也就意味着双精度浮点数最多存贮2^53份数字切片，如果超过了，你就得开始砍掉末尾的数字。比特币的2100万亿聪的总量，等于 2^50.899，刚好低于这个最大值。使双精度浮点数可以完美表示比特币。

**等量判断问题**

看下面的一段python代码

```python
print 0.1 + 0.1 == 0.2
print 0.1 + 0.2 == 0.3
```

结果第一行会输出 True，第二行会输出 False。为什么又这么蠢？这要从浮点数的表示方式说起，我们都知道计算机是用二进制来表示数字的，那小数的二进制是什么呢？我们使用乘二取整的方式来计算一下 0.1 的二进制表示（不会？其实我也是现查的小数如何转化为二进制）。

```
0.1 * 2 = 0.2 --> 0
0.2 * 2 = 0.4 --> 0
0.4 * 2 = 0.8 --> 0
0.8 * 2 = 1.6 --> 1
0.6 * 2 = 1.2 --> 1
0.2 * 2 = 0.4 --> 0
...
```

最后得出 0.1 的二进制表达是个无限循环小数 0.0001100110011...而且我们还发现 0.2，0.4，0.6，0.8 都在这个式子里，也就都是无限循环小数。那 0.1，0.3，0.7，0.9 只是他们的移一位，所以也都是无限循环小数。事实是，在这十个数中只有 0.0 和 0.5 可以用二进制精确的表示。为什么只有他俩？和进制的性质有关，这里就不去深究了。我们只需要知道，99.9999%（后面30个9）的浮点数都是不精确表示的，所以他们的运算结果也不可能精确表示，四舍五入后碰上了那是偶然。但是，计算机作为一个工具，只要满足我们的精度需求也就可以了。所以我们可以自己写一个对浮点数进行等量判断的函数，先确定可接受的精确度范围，如果误差在可接受的范围内，我们就认为相等。总之，不要直接对浮点数进行等量判断。

### 字符和字符串

**避免神秘字符串**

看下面一个例子

``` python
def next_motion(ball_handler, ...):
    if ball_handler == 'YOTTABYTE 95':
        run_to_week_side()
    ...
```

这次的篮球机器人识别到的是球衣上的所有字符串。。总之可读性和鲁棒性是所有神秘值得共同问题。除此之外，产品的国际化策略应该越早考虑越好，如果考虑需要国际化，本书建议把所有字符串都保存在外部资源中，并为每一种语言创建单独的版本。

**编码使用 Unicode**

对于中文来说，Unicode 是最普遍也是最好的编码方式，但是很多人都会被字符编码问题搞的团团转，我就有类似的经历。当输入输出的编码需求变化比较多时，建议的处理方式是，在程序中把所有的字符串都保存为一种格式，比如 Unicode， 同时在尽可能靠近输入和输出的位置做相对应的格式转换。

**Java 的字符串处理**

String 在 Java 中并不是一个基本类型，而是一个不可变的 final Class。每次修改或者重新赋值其实都是 new 了一个新的对象。但由于是引用变量，这同样会引起双等号无效的问题，因此在 Java 中我们通常使用 equals() 函数来比较两个字符串。其逻辑是对比同位置的每个 char。对字符串进行频繁操作也是一个性能较低的方式，于是我们通常使用 StringBuffer 和 StringBuilder 类代替完成这些任务，具体的区别这里就不讲了。我觉得 Java 的限制规则还是有点多，所以让人觉得不太好用。

另外提一下，Java 中储存密码一般还是使用 char[] 来代替 String。安全性仍然是主要原因。虽然在 String 加载密码之后可以把这个变量扔掉，但是字符串并不会马上被 GC 回收，一但进程在 GC 执行到这个字符串之前被 dump，dump 出的的转储中就会含有这个明文的字符串。char[] 则不会有这个问题。

### 布尔变量

**没什么好讲的**

布尔变量简单到没什么好讲的，使用方式也很少有坑。但我在搜寻资料时找到的两个建议，觉得还挺实用的：

1. 用布尔变量简化复杂的判断表达式
2. 程序的参数尽量避免使用布尔变量，降低可读性

**python强制转换的坑**

在自己写代码的时候遇到一个挺烦的坑，下面的语句会输出 True。

```
bool('False')
```

这是因为 bool 型的强制转换会把所有非空的字符串转化为 True，而 ‘False’ 是一个非空字符串。
解决办法是使用 eval() 函数，不过 eval 有 eval 的坑……不细聊。

### 枚举类型

**没什么好讲的**

枚举类型也没什么好讲的，使用枚举代替基本类型的好处主要有：

1. 增加代码可读性
2. 编译器的检查更严格

**Java 使用 switch 时注意**

Java 又来了，我之前使用 switch 判断枚举类型的值时发现的一个坑。看这段代码

```java
private boolean isMeetingRoomAvailable(RZYMeetingRoom meetingRoom){
    boolean result = true;

    switch (meetingRoom){
        case RZYMeetingRoom.ZettaByte:
            // do something
            break;
        case RZYMeetingRoom.PetaByte:
            // do something
            break;
        case RZYMeetingRoom.TeraByte:
            // TeraByte has been occupied forever
            result = false;
            break;
        case RZYMeetingRoom.ExaByte:
            // do something
            break;
        case RZYMeetingRoom.YottaByte:
            // do something
            break;
    }
    return result;
}
```

乍一看没问题，但是运行起来会报错。原因是在 case 取情况时，不可以使用 RZYMeetingRoom.ZettaByte，而应该直接写本身的值 ZettaByte。这与用双等号判断时是不同的，没法说，这就是我为什么不用 Java。

## 不常见的数据类型

本书讨论的不常见类型主要是结构体，指针和全局数据。这在现代语言中确实很少被用到或者基本过时，甚至很多面向对象的教材中都没有提到过结构体，那我们为什么还要讲呢？因为这一章就叫做不常见的数据类型。

### 结构体

结构体是一个由其他类型数据组成的数据。也可以由只包含公共的数据成员，不包含子程序的类来实现。

你可能会问，那我们直接用类多好？还可以提供私密性和功能性，你说的没错，想用类就用类好了，没什么区别。但是C语言没有类。当你发现你在写C这种啥也没有的纯粹语言时，自由度会上升一个档次。

所以结构体的优点就是类的优点：数据关系明确，简化数据块的操作，减少代码的维护。

例子就不举了。

### 指针

我们重点来讲一下指针。可能你的语言不要求你使用指针，但是理解指针也有助于理解你的编程语言是如何工作的。

我最开始看到这里的时候也比较懵逼，指针为什么放在数据类型的章节里？学习之后才有所了解，其实指针就是一种数据类型。为什么这么说呢？我们来看一段复杂的代码。

```c
int x = 95;
int * p = &x;
```

上面的式子很好理解，int 是数据类型，变量名是 x，值是 95。其实一个指针的初始化也是这样的。值是 x 的地址，变量名是 p，数据类型就是整型指针 int *。这个 * 写在哪里其实都可以，但是要理解的是，最终成为指针的这个变量叫做 p 而不是 *p。如果我分开写这个初始化式子的话应该是下面这样的：

```c
int * p;
p = &x;
```

所以指针其实就是一种数据类型，而且我们提“指针”的时候就像是在提“数值类型”，后者包括整型，浮点型等等，前者则包括整型指针，浮点型指针等等。我们在声明指针时，要知道指针指向的地址所存的内容是什么，也就是要明确它的基本类型。

还是想简单画一个图来解释一下什么是指针。

<center><img src="/images/blog/basic_data_type_pointer_illustraion.png"></center>

首先声明一个整型变量 x，编译器会为它分配一个唯一的内存单元用于储存数据。这里则是地址为 1707 的内存单元。然后给 x 赋值 95，则内存单元中就会储存一个整型数值（不管它是怎么表示的，反正是 95 这个数本身）。接着我们声明一个整型指针变量，系统再为它分配一个随机的内存单元，比如 1702。然后为这个指针变量赋值为 x （第一个字节）的地址，这个地址就存入 1702 内存中。那 \*p 是什么呢？* 是对指针的一种操作符，表示取指针 p 指向的地址里的值。于是现在 p 和 &x 都等于 1707，*p 和 x 都等于 95。这就是指针的意义。形象的解释就是，有个人去 1702 想找秋实，然后他们会说，你去 1707 找，然后就找到了。。。不严谨不严谨。

既然指针也是一种数据类型，那么就会有一些定义好的基础操作，比如加减就是在内存地址中向右或者向左移动一个类型单元。这就是为什么数组可以用指针来表示，因为数组的指针指向的就是数组第一个元素第一个字节的内存地址。

可是指针有什么用呢？我们发现 & 也可以调出地址来啊。其实指针相当于把 & 调出来的地址储存了下来并可以随意变化，起到了一些特别牛逼的作用：

1. 函数调用时只传地址（一个指针），而不用传整份数据
2. 避免副本和共享数据，不用每次都创建副本

我们用一个例子来理解这两个作用，假设球队来了个新人，也穿 95 号球衣，然后打球比秋实厉害，秋实就得给让啊，策略是把自己的球号加1。

```c
void change_jersey_number(int jersey_number){
    jersey_number = jersey_number + 1;
}

int main(){
    int qs_jersey_number = 95;
    change_jersey_number(qs_jersey_number);
    printf("当前球衣号为：%d \n", qs_jersey_number);
    return 0;
}
```

但是很明显，程序的输出依然是 95。因为我们在子程序 change_jersey_number 中操作时，传进来的参数仅仅是一个副本，也就是说，程序为 jersey_number 这个变量随机分配了一个地址（假设是 1702），然后传参时将 qs_jersey_number 的值复制到这个地址中，对这个临时的内存空间进行了操作，子程序结束后再释放掉。整个过程对真正的 qs_jersey_number 毫无影响。形象的解释是，我们在 1702 复制了一个秋实，让他换了球衣，再销毁他（emmm这个例子不太好），对真正的秋实并没有影响。而且，复制一个秋实的代价是很大的，会引起安全性的问题。那如果我们改用指针操作呢？代码如下

```c
void change_jersey_number(int *jersey_number){
    *jersey_number = *jersey_number + 1;
}

int main(){
    int qs_jersey_number = 95;
    change_jersey_number(&qs_jersey_number);
    printf("当前球衣号为：%d \n", qs_jersey_number);
    return 0;
}
```

这一次，1702 里住了一个指针，在传参时传入秋实的房间号，指针会直接告诉秋实本人让他换球衣，这样就避免了创建副本的操作。所以用指针的主要原因是让函数共享存储器，一个函数可以修改另一个函数创建的数据，只要提供数据在内存中的地址。

指针的作用就讲到这里，其实用得好可以极大地提升程序的性能。那么为什么好多语言都没有指针了？就是因为大家都用不好指针，所以被封装为了更高级的设计，指针依然还是存在的，只不过大多数时候不需要编程人员了解了。但如果你是一个C语言程序员，你是逃不掉的。本书给了以下几个使用指针的建议。

1. **把指针操作写在子程序里：** 减少访问指针代码位置的数量，也就减少了犯错的可能性。
2. **在相同的作用域中分配和释放指针：** 保证指针分配与释放的对称性。
3. **用额外的指针提高代码清晰度：** 如果多用一个指针可以使逻辑更清晰，那就用。比如链表节点插入的例子，可以自己查一下看看。
4. **按照正确顺序删除链表中的指针：** 避免删除某个指针后导致某些地址无法访问。
5. **在删除或释放指针后把他们设为空值：** 这样可以保证你向一个空悬指针（删除或释放后的指针）写入数据时会报错，从而避免了空悬指针带来的更大错误。
6. **放弃使用指针：** 如果你用不明白，那不如不用，找其他的替代方法。

### 全局数据

全局数据是在程序最上层的数据，代码任何位置都可以直接访问的数据类型。这个东西优点缺点都比较好理解，所以简单的过一下即可。本书的建议是，全局数据能不用就不用，真想用的话也用访问器子程序封装后再使用，而不是直接操作全局变量。

使用全局数据的缺点：

1. 无意间的修改造成冲突
2. 命名冲突
3. 并发访问的问题
4. 模块初始化的顺序影响较大
5. 阻碍了代码的复用
6. 干扰了模块化

什么时候可以使用全局数据：

1. 全局的配置项
2. 模拟枚举类型
3. 消除流浪数据（那些跨层级传递的参数，而中间某些层级并不需要它）

如果一定要使用全局数据的话：

1. 先看看能不能用局部变量或类变量代替
2. 明确你用的语言的全局变量命名规则
3. 写文档说明
4. 不更改、不传递

\- END -