---
layout: wiki
title: LaTeX
categories: LaTeX
description: LaTeX数学符号和排版
keywords: LaTeX
---

总结一下使用LaTeX书写数学公式时常用的语法，不包括排版。

## **函数、符号及特殊字符**

### **声调**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\bar{x}</td>
<td><img alt="\bar{x}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/9/4/c947a5bcc06592f37f6b1c4f2ed57dea.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\acute{\eta}</td>
<td><img alt="\acute{\eta}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/f/f/8ff055145396a2ffefacea0b18ec3fda.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\check{\alpha}</td>
<td><img alt="\check{\alpha}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/c/4/ac4a31ee5874dc5044590eedae7a48c4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\grave{\eta}</td>
<td><img alt="\grave{\eta}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/1/f/91f1cf98709ee5bd4380b05d04ce260a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\breve{a}</td>
<td><img alt="\breve{a}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/5/58565c69fa6e895ea11e57ffdbe7d4cd.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\ddot{y}</td>
<td><img alt="\ddot{y}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/7/58779ff5e3932c43545a8d8114384dd6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\dot{x}</td>
<td><img alt="\dot{x}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/4/584bdd6bbf3b22901631c94c12f09332.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\hat{\alpha}</td>
<td><img alt="\hat{\alpha}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/f/e/3fe9b211473065676e1b8048e21b9743.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\tilde{\iota}</td>
<td><img alt="\tilde{\iota}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/d/b/5db129ecac03423d19e453d9ada8a0e8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **函数**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\sin\theta</td>
<td><img alt="\sin\!\theta" src="http://upload.wikimedia.org/wikipedia/zh/math/0/9/3/09370ac60fb75f6555aad6ce6fa51284.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\cos\theta</td>
<td><img alt="\cos\!\theta" src="http://upload.wikimedia.org/wikipedia/zh/math/3/9/2/3922f2c5f59efde904a8e70433e3c014.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\tan\theta</td>
<td><img alt="\tan\!\theta" src="http://upload.wikimedia.org/wikipedia/zh/math/8/9/e/89eb6b1450d9b26d2071d1f64a567aa4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\arcsin\frac{L}{r}</td>
<td><img alt="\arcsin\frac{L}{r}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/9/c/59c47fbda47ed6da13841e777d49dd4e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\arccos\frac{T}{r}</td>
<td><img alt="\arccos\frac{T}{r}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/9/b/79bed5fd8aa7405d98f639dd1dfbb427.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\arctan\frac{L}{T}</td>
<td><img alt="\arctan\frac{L}{T}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/7/1/97143846d4543215119d569364979c2a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\sinh g</td>
<td><img alt="\sinh\!g" src="http://upload.wikimedia.org/wikipedia/zh/math/6/6/2/662b4f90832dea02dcee532c226df3bf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\cosh h</td>
<td><img alt="\cosh\!h" src="http://upload.wikimedia.org/wikipedia/zh/math/0/b/9/0b95b10be34e368fea4697a333f14c5d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\tanh i</td>
<td><img alt="\tanh\!i" src="http://upload.wikimedia.org/wikipedia/zh/math/d/7/7/d779acc41d8d9e1b708644807d2b61a1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\operatorname{sh}j</td>
<td><img alt="\operatorname{sh}j" src="http://upload.wikimedia.org/wikipedia/zh/math/d/9/a/d9a5b98974c7360119bf868fc1c5c544.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\operatorname{argsh}k</td>
<td><img alt="\operatorname{argsh}k" src="http://upload.wikimedia.org/wikipedia/zh/math/c/4/4/c44c117b43a78dba43cbd0d47f9ae9e7.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\operatorname{ch}h</td>
<td><img alt="\operatorname{ch}h" src="http://upload.wikimedia.org/wikipedia/zh/math/9/b/e/9becb1baaf3ac62c35e5ecd33c689cee.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\operatorname{argch}l</td>
<td><img alt="\operatorname{argch}l" src="http://upload.wikimedia.org/wikipedia/zh/math/e/1/3/e13362fecb2c9c535e6370bed2355f20.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\operatorname{th}i</td>
<td><img alt="\operatorname{th}i" src="http://upload.wikimedia.org/wikipedia/zh/math/8/1/4/8146bd5925b931e7ffe878c83762a945.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\operatorname{argth}m</td>
<td><img alt="\operatorname{argth}m" src="http://upload.wikimedia.org/wikipedia/zh/math/5/5/3/5536490854b0c2592644c44455cfd43a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>k'(x)=\lim_{\Delta x\to 0}\frac{k(x)-k(x-\Delta x)}{\Deltax}</td>
<td><img alt="k'(x)=\lim_{\Delta x\to0}\!\frac{k(x)-k(x-\Delta x)}{\Delta x}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/3/5/a35afcec7be6f2e0e49964f3997eeac6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\limsup S</td>
<td><img alt="\limsup S" src="http://upload.wikimedia.org/wikipedia/zh/math/c/3/a/c3ac735451511bdf8de1d5da58206a8a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\liminf I</td>
<td><img alt="\liminf I" src="http://upload.wikimedia.org/wikipedia/zh/math/f/8/5/f8508b1afb27fe30fd5be91984938df4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\max H</td>
<td><img alt="\max\!H" src="http://upload.wikimedia.org/wikipedia/zh/math/9/9/c/99ced9d4b2ceaa766c3c5d68bac86979.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\min L</td>
<td><img alt="\min\!L" src="http://upload.wikimedia.org/wikipedia/zh/math/0/7/d/07ddfdd950e34d4440b5b67678ad8bfa.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\inf s</td>
<td><img alt="\inf s" src="http://upload.wikimedia.org/wikipedia/zh/math/7/4/8/7487ba38d7669bd75d98d64352f0e180.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\sup t</td>
<td><img alt="\sup t" src="http://upload.wikimedia.org/wikipedia/zh/math/6/5/3/653854c1aad8cfa165b5a8c39b5fb969.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\exp\!t</td>
<td><img alt="\exp\!t" src="http://upload.wikimedia.org/wikipedia/zh/math/c/8/e/c8e52278a8bc8c608afa285f7c4c28df.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\ln X</td>
<td><img alt="\ln\!X" src="http://upload.wikimedia.org/wikipedia/zh/math/9/f/6/9f6784ddb3f4b9555612f1de74098116.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\lg X</td>
<td><img alt="\lg\!X" src="http://upload.wikimedia.org/wikipedia/zh/math/3/2/6/3267adf708693ca43b8fc4dace597be0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\log X</td>
<td><img alt="\log\!X" src="http://upload.wikimedia.org/wikipedia/zh/math/1/6/d/16d14ffacc5feb0b4f30de46aea931bf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\log_\alpha X</td>
<td><img alt="\log_\alpha\!X" src="http://upload.wikimedia.org/wikipedia/zh/math/b/b/6/bb6db979b913638a0d0f30a4ac32bd42.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\ker x</td>
<td><img alt="\ker x" src="http://upload.wikimedia.org/wikipedia/zh/math/c/a/0/ca051c4eda4d55ca99bd3b918bd7ead5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\deg x</td>
<td><img alt="\deg\!x" src="http://upload.wikimedia.org/wikipedia/zh/math/f/b/5/fb5d0a3b0f1fec9639c04e92b252fee0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\gcd(T,U,V,W,X)</td>
<td><img alt="\!\gcd(T,U,V,W,X)" src="http://upload.wikimedia.org/wikipedia/zh/math/e/d/8/ed810992e880412f54389f581b3e4f3c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\Pr x</td>
<td><img alt="\Pr x" src="http://upload.wikimedia.org/wikipedia/zh/math/1/f/1/1f1c9533b66b3af1a2540bfa41ca9dff.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\det x</td>
<td><img alt="\det\!x" src="http://upload.wikimedia.org/wikipedia/zh/math/f/0/1/f011b7de0181e313c4e36293419bc4da.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\hom x</td>
<td><img alt="\hom x" src="http://upload.wikimedia.org/wikipedia/zh/math/9/1/9/919603d21a66d6909953cf095d8ce8c7.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\arg x</td>
<td><img alt="\arg x" src="http://upload.wikimedia.org/wikipedia/zh/math/4/2/8/428ef2e44e64d5de3773f591de3d5e06.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\dim x</td>
<td><img alt="\dim x" src="http://upload.wikimedia.org/wikipedia/zh/math/f/1/b/f1b92c71934d2d660f68777740560aa9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\lim_{t\to n}T</td>
<td><img alt="\lim_{t\to n}T" src="http://upload.wikimedia.org/wikipedia/zh/math/7/a/b/7ab3a88998975fc6c02f395eb7a677cc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **同余**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\pmod{m}</td>
<td><img alt="\pmod{m}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/6/8/1680ea379fd6694b28ae04a34e77d8e6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>a \bmod b</td>
<td><img alt="a \bmod b" src="http://upload.wikimedia.org/wikipedia/zh/math/5/4/e/54efbc7c212108a4011e84c69cdd91f8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **微分**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
</tr>
<tr>
<td>\nabla</td>
<td><img alt="\nabla" src="http://upload.wikimedia.org/wikipedia/zh/math/f/e/3/fe3a83e41074834731743ab803cd4936.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\partial x</td>
<td><img alt="\partial x" src="http://upload.wikimedia.org/wikipedia/zh/math/2/8/d/28ddb3e82115d069796faf6356e2dbf6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\mathrm{d}x</td>
<td><img alt="\mathrm{d}x\ " src="http://upload.wikimedia.org/wikipedia/zh/math/3/d/7/3d7524d2b2372a1188d73b20b9ba4b31.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\dot x</td>
<td><img alt="\dot x" src="http://upload.wikimedia.org/wikipedia/zh/math/3/a/b/3abf2ac2fcc14362b32b0411d43cbf48.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\ddot y</td>
<td><img alt="\ddot y" src="http://upload.wikimedia.org/wikipedia/zh/math/0/d/2/0d23f3a6391ae79fac3f4b30ec914a84.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
&nbsp;</td>
<td>&nbsp;</td>
</tr>
</tbody>
</table></div>

### **集合**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
</tr>
<tr>
<td>\forall</td>
<td><img alt="\forall" src="http://upload.wikimedia.org/wikipedia/zh/math/d/4/d/d4d49bead125261b226eaa867bd016ce.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\exists</td>
<td><img alt="\exists" src="http://upload.wikimedia.org/wikipedia/zh/math/9/3/e/93ebe8636e1f8d60004fe33d1321674e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\empty</td>
<td><img alt="\empty" src="http://upload.wikimedia.org/wikipedia/zh/math/4/d/f/4df085f70a97244c977b6ff20b1952b4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\emptyset</td>
<td><img alt="\emptyset" src="http://upload.wikimedia.org/wikipedia/zh/math/4/d/f/4df085f70a97244c977b6ff20b1952b4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\varnothing</td>
<td><img alt="\varnothing" src="http://upload.wikimedia.org/wikipedia/zh/math/d/0/9/d096fc15d57854ec89d746709b02e52e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\in</td>
<td><img alt="\in" src="http://upload.wikimedia.org/wikipedia/zh/math/8/c/2/8c20c78b364ed5dbadd49e5b997aa1cc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\ni</td>
<td><img alt="\ni" src="http://upload.wikimedia.org/wikipedia/zh/math/7/c/3/7c34bf8e7b41952d024ef2180330b308.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\not\in</td>
<td><img alt="\not\in" src="http://upload.wikimedia.org/wikipedia/zh/math/5/2/5/525f6840d78cdc4bcb177f06c7964022.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\notin</td>
<td><img alt="\notin" src="http://upload.wikimedia.org/wikipedia/zh/math/6/9/2/692614f72e231db0d2313050ac29e113.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\subset</td>
<td><img alt="\subset" src="http://upload.wikimedia.org/wikipedia/zh/math/7/a/f/7afa88c2877d79e6a8a190b360edfcd6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\subseteq</td>
<td><img alt="\subseteq" src="http://upload.wikimedia.org/wikipedia/zh/math/a/0/7/a07903a0504f50f27e2a85c27e47fbd5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\supset</td>
<td><img alt="\supset" src="http://upload.wikimedia.org/wikipedia/zh/math/0/f/2/0f2c04f82a1eb8e3e371366214579f5b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\supseteq</td>
<td><img alt="\supseteq" src="http://upload.wikimedia.org/wikipedia/zh/math/5/5/f/55fef34436f901c3e488cbaa41050df8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\cap</td>
<td><img alt="\cap" src="http://upload.wikimedia.org/wikipedia/zh/math/e/7/8/e78f632038354aae583f795a73d4e6b8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\bigcap</td>
<td><img alt="\bigcap" src="http://upload.wikimedia.org/wikipedia/zh/math/d/d/f/ddf86464dcc2190258c76ddc1da7032a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\cup</td>
<td><img alt="\cup" src="http://upload.wikimedia.org/wikipedia/zh/math/4/3/2/432c1df69e11aba7c5c5070e7578609f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\bigcup</td>
<td><img alt="\bigcup" src="http://upload.wikimedia.org/wikipedia/zh/math/8/d/5/8d50523fd64ca129ae09c7ae73e1385f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\biguplus</td>
<td><img alt="\biguplus" src="http://upload.wikimedia.org/wikipedia/zh/math/9/0/2/902effd4844ae7dbd71f9f3cecec25f0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\sqsubset</td>
<td><img alt="\sqsubset" src="http://upload.wikimedia.org/wikipedia/zh/math/f/2/2/f22614b2c39be672bfda11afddd15c18.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\sqsubseteq</td>
<td><img alt="\sqsubseteq" src="http://upload.wikimedia.org/wikipedia/zh/math/b/1/b/b1be6c28d38e18390ea808e56c4e1d93.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\sqsupset</td>
<td><img alt="\sqsupset" src="http://upload.wikimedia.org/wikipedia/zh/math/f/e/4/fe47401f278fa0892559bad5b9373ebe.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\sqsupseteq</td>
<td><img alt="\sqsupseteq" src="http://upload.wikimedia.org/wikipedia/zh/math/0/9/a/09a87c18c45c26e284e6160bc344ebe9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\sqcap</td>
<td><img alt="\sqcap" src="http://upload.wikimedia.org/wikipedia/zh/math/5/9/5/59553260bed5e399db651cf2a3f703cf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\sqcup</td>
<td><img alt="\sqcup" src="http://upload.wikimedia.org/wikipedia/zh/math/2/d/1/2d130618c4d29b0f1f52f248ff359341.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\bigsqcup</td>
<td><img alt="\bigsqcup" src="http://upload.wikimedia.org/wikipedia/zh/math/b/f/6/bf60615860b12ad8b31cc27645fc5224.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **逻辑**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
<th style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
语法</th>
<th>效果</th>
</tr>
<tr>
<td>p</td>
<td><img alt="p" src="http://upload.wikimedia.org/wikipedia/zh/math/8/3/8/83878c91171338902e0fe0fb97a8c47a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\land</td>
<td><img alt="\land" src="http://upload.wikimedia.org/wikipedia/zh/math/9/c/a/9cae4437756a15b8e44ec23e07fb1f65.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\wedge</td>
<td><img alt="\wedge" src="http://upload.wikimedia.org/wikipedia/zh/math/1/b/a/1ba4f06f68614e5da79a8ebd378d532a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\bigwedge</td>
<td><img alt="\bigwedge" src="http://upload.wikimedia.org/wikipedia/zh/math/6/c/1/6c1357f344d79b14bbd6a43c112f36db.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\bar{q} \to p</td>
<td><img alt="\pagecolor{White} \bar{q} \to p" src="http://upload.wikimedia.org/wikipedia/zh/math/6/c/c/6cc8a80363dc8031c53a0f4ae4704c91.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\lor</td>
<td><img alt="\lor" src="http://upload.wikimedia.org/wikipedia/zh/math/5/a/d/5addb134385e47a2efa484f6306e75a1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\vee</td>
<td><img alt="\vee" src="http://upload.wikimedia.org/wikipedia/zh/math/7/2/7/727ea4c8c49862411edae46adf506e3e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\bigvee</td>
<td><img alt="\bigvee" src="http://upload.wikimedia.org/wikipedia/zh/math/a/f/2/af2beebc69c64f6a9a59db61113e14a0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\lnot</td>
<td><img alt="\lnot" src="http://upload.wikimedia.org/wikipedia/zh/math/8/e/f/8efca960b209402104b448a5ad9486a8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\neg q</td>
<td><img alt="\pagecolor{White} \neg q" src="http://upload.wikimedia.org/wikipedia/zh/math/d/8/a/d8a41edda094745ef7850fe97ceaa5ca.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\setminus</td>
<td><img alt="\setminus" src="http://upload.wikimedia.org/wikipedia/zh/math/1/7/d/17d233e7f25e7e6108e6e8135fc5bf65.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="border-left-width:2px; border-left-style:solid; border-left-color:rgb(170,170,170)">
\smallsetminus</td>
<td><img alt="\pagecolor{White} \smallsetminus" src="http://upload.wikimedia.org/wikipedia/zh/math/7/2/9/7290ff3fe4f3ef8927caf56dc3c2d131.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **根号**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\sqrt{3}</td>
<td><img alt="\sqrt{3}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/7/c/17c68e294ba0dc1356295bac633bf868.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\sqrt[n]{3}</td>
<td><img alt="\pagecolor{White}\sqrt[n]{3}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/7/7/f77bdd840c6d77e25f5c88640bf0ffbf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **关系符号**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td><code>\Delta ABC\sim\Delta XYZ</code></td>
<td><img alt="\Delta ABC\sim\Delta XYZ\!" src="http://upload.wikimedia.org/wikipedia/zh/math/6/a/3/6a3e77cae79f0fdcc1727b5061411221.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\sqrt{3}\approx1.732050808\ldots</code></td>
<td><img alt="\sqrt{3}\approx1.732050808\ldots" src="http://upload.wikimedia.org/wikipedia/zh/math/d/a/7/da73a49927110231f6021c6adb08a43d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\simeq</td>
<td><img alt="\simeq" src="http://upload.wikimedia.org/wikipedia/zh/math/8/e/3/8e3648e8286c414a11b8f10a833d5596.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\cong</td>
<td><img alt="\cong" src="http://upload.wikimedia.org/wikipedia/zh/math/f/1/6/f16a7bd80bb5648a755eb58221d03546.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\dot=</td>
<td><img alt="\dot=" src="http://upload.wikimedia.org/wikipedia/zh/math/e/0/1/e011dac23072797e8fc73cf575709782.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\ggg</code></td>
<td><img alt="\ggg" src="http://upload.wikimedia.org/wikipedia/zh/math/f/b/7/fb7d1cf9a5e65f98089b6b2cb1570a3c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\gg</code></td>
<td><img alt="\gg" src="http://upload.wikimedia.org/wikipedia/zh/math/3/3/e/33e3502dfbd3f875dcbdd2f9a40eedb4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>&gt;</code></td>
<td><img alt=">\," src="http://upload.wikimedia.org/wikipedia/zh/math/1/1/4/114529aa81593e4dfb2279a9b594c779.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\ge</code></td>
<td><img alt="\ge" src="http://upload.wikimedia.org/wikipedia/zh/math/8/f/b/8fbe2a506fe3db0835548e1b648ec977.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\geqq</code></td>
<td><img alt="\geqq" src="http://upload.wikimedia.org/wikipedia/zh/math/2/3/e/23e68b97e8ddf443cdeed5ce45e04abe.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>=</code></td>
<td><img alt="=\," src="http://upload.wikimedia.org/wikipedia/zh/math/4/4/8/4488ba5f7e82e2d8c136b559d95283d5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\leq</code></td>
<td><img alt="\leq" src="http://upload.wikimedia.org/wikipedia/zh/math/4/9/d/49dc1443f33cf63082d6e193dd2af78f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\leqq</code></td>
<td><img alt="\leqq" src="http://upload.wikimedia.org/wikipedia/zh/math/8/8/5/885f9db7c38c45758c0f7b07b823bc64.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>&lt;</code></td>
<td><img alt="<\," src="http://upload.wikimedia.org/wikipedia/zh/math/0/1/6/0164cc2c31c906d9d775037410cc195c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\ll</code></td>
<td><img alt="\ll" src="http://upload.wikimedia.org/wikipedia/zh/math/9/4/3/9439146cc81e763e0563ccbbcb523314.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\lll</code></td>
<td><img alt="\lll" src="http://upload.wikimedia.org/wikipedia/zh/math/4/e/8/4e8dc43a1f5be9ea3d8d27fdea882497.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>(x-y)^2\equiv(-x+y)^2\equiv x^2-2xy+y^2</code></td>
<td><img alt="(x-y)^2\equiv(-x+y)^2\equiv x^2-2xy+y^2" src="http://upload.wikimedia.org/wikipedia/zh/math/6/c/9/6c9a2bfd0d3b9a5a74f8682479733cf9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<p><code>\begin{align}</code></p>
<p><code>\because\begin{cases}</code></p>
<p><code>\acute{a}x^2+bx^2+c\gtrless0\gtrless\grave{a}x^2+bx^2+c\\</code></p>
<p><code>\acute{a}&gt;0&gt;\grave{a}</code></p>
<p><code>\end{cases}\\</code></p>
<p><code>\therefore\frac{-b\pm\sqrt{b^2-4\acute{a}c}}{2\acute{a}}{}_\lessgtr^\gtrlessx_\lessgtr^\gtrless\frac{-b\pm\sqrt{b^2-4\grave{a}c}}{2\grave{a}}</code></p>
<p><code>\end{align}</code></p>
</td>
<td><img alt=" \begin{align} \because\begin{cases} \acute{a}x^2+bx^2+c\gtrless0\gtrless\grave{a}x^2+bx^2+c\ \acute{a}>0>\grave{a} \end{cases}\ \therefore\frac{-b\pm\sqrt{b^2-4\acute{a}c}}{2\acute{a}}{}_\lessgtr^\gtrless x_\lessgtr^\gtrless\frac{-b\pm\sqrt{b^2-4\grave{a}c}}{2\grave{a}} \end{align} " src="http://upload.wikimedia.org/wikipedia/zh/math/8/1/0/8105aed2a6a0372d348af577ea8652d8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>x\not\equiv N</td>
<td><img alt="x\not\equiv N" src="http://upload.wikimedia.org/wikipedia/zh/math/1/b/0/1b05bef638197b56e7298f7ce316ad13.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>x\ne A</td>
<td><img alt="x\ne A" src="http://upload.wikimedia.org/wikipedia/zh/math/3/1/0/3104de4e8ef189be10d43d6ca8e9444a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>x\neq C</td>
<td><img alt="x\neq C" src="http://upload.wikimedia.org/wikipedia/zh/math/7/0/1/7016f46da82d8566a65d93a0ed082874.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>t\propto v</td>
<td><img alt="t\propto v" src="http://upload.wikimedia.org/wikipedia/zh/math/c/f/f/cfff18dbfebc64e8d6080fa3731249c1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\pm</td>
<td><img alt="\pm" src="http://upload.wikimedia.org/wikipedia/zh/math/5/7/2/5722e2f6169308b8be3542900c6d6553.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\mp</td>
<td><img alt="\mp" src="http://upload.wikimedia.org/wikipedia/zh/math/0/2/f/02f4d839cf96b60132fea53480d63648.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **几何符号**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th colspan="2">特征</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td colspan="2">菱形</td>
<td>\Diamond</td>
<td><img alt="\Diamond" src="http://upload.wikimedia.org/wikipedia/zh/math/6/a/2/6a2084de787fb2d1c3e408d926425904.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td colspan="2">正方形</td>
<td>\Box</td>
<td><img alt="\Box" src="http://upload.wikimedia.org/wikipedia/zh/math/9/d/8/9d8f6d53ad070771a6910933810023c4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">三角形</td>
<td>Delta</td>
<td><code>\Delta</code></td>
<td><img alt="\Delta\!" src="http://upload.wikimedia.org/wikipedia/zh/math/5/a/b/5abc9a983cecde2f902ff5e4de34ec1f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>图型</td>
<td><code>\triangle</code></td>
<td><img alt="\triangle" src="http://upload.wikimedia.org/wikipedia/zh/math/f/5/d/f5d889f32d6794e1bc2ed394e9688c76.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td colspan="2">角名</td>
<td><code>\angle\Alpha\Beta\Gamma</code></td>
<td><img alt="\angle\Alpha\Beta\Gamma" src="http://upload.wikimedia.org/wikipedia/zh/math/3/8/5/38501930aadb2f2d724c193f209f9578.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td colspan="2"><a target="_blank" href="http://zh.wikipedia.org/wiki/%E8%A7%92%E5%BA%A6" rel="nofollow" title="角度" style="color:rgb(106,57,6); text-decoration:none">角度</a></td>
<td><code>\sin\!\frac{\pi}{3}=\sin60^\operatorname{\omicron}=\frac{\sqrt{3}}{2}</code></td>
<td><img alt="\sin\!\frac{\pi}{3}=\sin60^\operatorname{\omicron}=\frac{\sqrt{3}}{2}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/a/0/da0804e5be1869c583e761bb38e2f007.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td colspan="2"><a target="_blank" href="http://zh.wikipedia.org/wiki/%E5%9E%82%E7%9B%B4" rel="nofollow" title="垂直" style="color:rgb(106,57,6); text-decoration:none">垂直</a></td>
<td>\perp</td>
<td><img alt="\perp" src="http://upload.wikimedia.org/wikipedia/zh/math/d/2/1/d21e3d53f78769beee8ff7b6c4a9a92c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **箭头符号**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\leftarrow</td>
<td><img alt="\leftarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/a/6/4/a6465c0244621c63e7e1e96eb55aad7a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\gets</td>
<td><img alt="\gets" src="http://upload.wikimedia.org/wikipedia/zh/math/c/e/9/ce9bfd92570656019fed79d092b6ae74.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\rightarrow</td>
<td><img alt="\rightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/8/3/e/83e37b7246fdfcb99b2754210ebeae27.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\to</td>
<td><img alt="\to" src="http://upload.wikimedia.org/wikipedia/zh/math/d/a/5/da558173e1f2ddfeb273751d481f9a52.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\leftrightarrow</td>
<td><img alt="\leftrightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/1/b/1/1b18a4c4fc578ef4cfd1cc0eb0daa473.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\longleftarrow</td>
<td><img alt="\longleftarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/5/7/f/57f18f6115ac560cb869f55d691ab334.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\longrightarrow</td>
<td><img alt="\longrightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/b/7/8/b78286a473d99ba959caf406cea7e493.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\mapsto</td>
<td><img alt="\mapsto" src="http://upload.wikimedia.org/wikipedia/zh/math/9/4/5/9450612598aafa1f56196840d7f83ff9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\longmapsto</td>
<td><img alt="\longmapsto" src="http://upload.wikimedia.org/wikipedia/zh/math/b/6/8/b68c87df100d6a59aea8e716bb3a97ce.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\hookrightarrow</td>
<td><img alt="\hookrightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/7/2/9/7294bafcf0fbf24fa305a03ddb7bd367.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\hookleftarrow</td>
<td><img alt="\hookleftarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/f/d/4/fd458e10f8ceba4e35d89bafa86905de.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\nearrow</td>
<td><img alt="\nearrow" src="http://upload.wikimedia.org/wikipedia/zh/math/3/0/f/30f1696dc98c430e93a6139c456dbd5d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\searrow</td>
<td><img alt="\searrow" src="http://upload.wikimedia.org/wikipedia/zh/math/7/5/2/75269e7e572c9cd78ae150d34a71b7d5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\swarrow</td>
<td><img alt="\swarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/5/f/b/5fb8d3e625fff8c3b4d6450236bad8eb.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\nwarrow</td>
<td><img alt="\nwarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/2/3/a/23ac812cbd7c1de7762b501b2575798a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\uparrow</td>
<td><img alt="\uparrow" src="http://upload.wikimedia.org/wikipedia/zh/math/f/0/4/f045028b3e31841b22efbbb9a0911dc0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\downarrow</td>
<td><img alt="\downarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/4/2/f/42f4ac9a26f75eda6a7716993026a6c8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\updownarrow</td>
<td><img alt="\updownarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/4/5/7/457ca7d9f0425e9b1dc99132e119dbce.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\rightharpoonup</td>
<td><img alt="\rightharpoonup" src="http://upload.wikimedia.org/wikipedia/zh/math/8/8/3/8837df45e6cc70b20f1c232847a27d71.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\rightharpoondown</td>
<td><img alt="\rightharpoondown " src="http://upload.wikimedia.org/wikipedia/zh/math/a/7/9/a79d180f700de8efbe9c9e44a53ad372.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\leftharpoonup</td>
<td><img alt="\leftharpoonup" src="http://upload.wikimedia.org/wikipedia/zh/math/4/8/9/4898039d7b0702b29079e5e9ca3c4513.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\leftharpoondown</td>
<td><img alt="\leftharpoondown " src="http://upload.wikimedia.org/wikipedia/zh/math/9/b/0/9b05a226682efc86dc1d66ef026ae2e3.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\upharpoonleft</td>
<td><img alt="\upharpoonleft" src="http://upload.wikimedia.org/wikipedia/zh/math/c/6/e/c6e4de1cefacd371ebbf050f78786be6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\upharpoonright</td>
<td><img alt="\upharpoonright " src="http://upload.wikimedia.org/wikipedia/zh/math/d/f/5/df58255d87a189b5c496160f06212765.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\downharpoonleft</td>
<td><img alt="\downharpoonleft" src="http://upload.wikimedia.org/wikipedia/zh/math/4/a/4/4a406771aef37db53572e672e9fcd360.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\downharpoonright</td>
<td><img alt="\downharpoonright" src="http://upload.wikimedia.org/wikipedia/zh/math/3/7/4/374d7e005ee1a76c99ac68f71028cbdc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\Leftarrow</td>
<td><img alt="\Leftarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/1/c/f/1cfb61f8b7206229c3ad6452e0d83674.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Rightarrow</td>
<td><img alt="\Rightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/d/f/0/df09aea884019cb88a2957126faba316.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Leftrightarrow</td>
<td><img alt="\Leftrightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/0/1/4/014cced2b73c22eb88cdc6901afb0c9d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\Longleftarrow</td>
<td><img alt="\Longleftarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/7/2/1/7218138eb9cfb7959782d4e553a9105e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Longrightarrow</td>
<td><img alt="\Longrightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/7/5/8/7585765360506206cb893e03b9517acc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Longleftrightarrow (or \iff)</td>
<td><img alt="\Longleftrightarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/3/5/c/35c86324cc425d53964bba41b40bbe99.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\Uparrow</td>
<td><img alt="\Uparrow" src="http://upload.wikimedia.org/wikipedia/zh/math/b/2/6/b267b68b9e6b5c95dc1853c82be33b00.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Downarrow</td>
<td><img alt="\Downarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/a/5/8/a5855048483c40e8ffeac0646476f178.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Updownarrow</td>
<td><img alt="\Updownarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/7/1/8/7185c13dd289c8bde5d575f846e9d521.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **特殊符号**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\eth</td>
<td><img alt="\eth" src="http://upload.wikimedia.org/wikipedia/zh/math/2/d/a/2dacecd4fffb3d4fdea52ed937b50c81.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\S</td>
<td><img alt="\S" src="http://upload.wikimedia.org/wikipedia/zh/math/5/d/6/5d60d7c05a80628104ef1bd0718eb3fc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\P</td>
<td><img alt="\P" src="http://upload.wikimedia.org/wikipedia/zh/math/8/9/9/899edd97aab272d0a8c8987321b24408.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\%</td>
<td><img alt="\%" src="http://upload.wikimedia.org/wikipedia/zh/math/2/8/f/28f423e28b5eb397034d51aaf59b708b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\dagger</td>
<td><img alt="\dagger" src="http://upload.wikimedia.org/wikipedia/zh/math/5/0/f/50f39cb506b81c04fb18893469de5be5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\ddagger</td>
<td><img alt="\ddagger" src="http://upload.wikimedia.org/wikipedia/zh/math/f/d/6/fd6bb9c23860e78a827828a896063b5b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\star</td>
<td><img alt="\star" src="http://upload.wikimedia.org/wikipedia/zh/math/2/3/d/23d64887f9c2add7a296e5b99acbbdfb.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>*</td>
<td><img alt="*" src="http://upload.wikimedia.org/wikipedia/zh/math/3/3/8/3389dae361af79b04c9c8e7057f60cc6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\ldots</td>
<td><img alt="\ldots" src="http://upload.wikimedia.org/wikipedia/zh/math/0/6/5/065775997fdbcb83ddbe8936e67e4f2c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\smile</td>
<td><img alt="\smile" src="http://upload.wikimedia.org/wikipedia/zh/math/e/c/9/ec97f8d0dbf2f26b882bb6d671d2e535.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\frown</td>
<td><img alt="\frown" src="http://upload.wikimedia.org/wikipedia/zh/math/4/f/8/4f8881ccda31a4b84283529b47d30c95.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\wr</td>
<td><img alt="\wr" src="http://upload.wikimedia.org/wikipedia/zh/math/b/5/c/b5ce93cb24555a53656581ff87bc2caf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\oplus</td>
<td><img alt="\oplus" src="http://upload.wikimedia.org/wikipedia/zh/math/b/7/1/b71edd70fcad670e99a9912ba5e55d77.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\bigoplus</td>
<td><img alt="\bigoplus" src="http://upload.wikimedia.org/wikipedia/zh/math/1/7/e/17e0badeeb2a6501df77203521a6501d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\otimes</td>
<td><img alt="\otimes" src="http://upload.wikimedia.org/wikipedia/zh/math/e/9/d/e9dd9013ec300ceba41484dfc2c9a876.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\bigotimes</td>
<td><img alt="\bigotimes" src="http://upload.wikimedia.org/wikipedia/zh/math/9/f/3/9f3cab49d684e7498a965b3e9d3c1524.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\times</td>
<td><img alt="\times" src="http://upload.wikimedia.org/wikipedia/zh/math/9/e/e/9eedd61e32f7a8e70e171028a7e5dc08.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\cdot</td>
<td><img alt="\cdot" src="http://upload.wikimedia.org/wikipedia/zh/math/3/6/f/36f8ae4c86b69d52d037a6802d91cc4a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\div</td>
<td><img alt="\div" src="http://upload.wikimedia.org/wikipedia/zh/math/a/3/9/a3933e4fee514b1dfa4cea09af6ae53e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\circ</td>
<td><img alt="\circ" src="http://upload.wikimedia.org/wikipedia/zh/math/1/0/c/10c3e97d2a3eda0d182b81d48f231b62.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\bullet</td>
<td><img alt="\bullet" src="http://upload.wikimedia.org/wikipedia/zh/math/b/f/5/bf588c17a2f1ba670dd67abd8ef6b8c6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\bigodot</td>
<td><img alt="\bigodot" src="http://upload.wikimedia.org/wikipedia/zh/math/9/6/a/96a7b9d0ce387adfe7c6f3b873a0b76a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\boxtimes</td>
<td><img alt="\boxtimes" src="http://upload.wikimedia.org/wikipedia/zh/math/e/2/2/e2211456bb3ab339c66e0ae2e2a813a4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\boxplus</td>
<td><img alt="\boxplus" src="http://upload.wikimedia.org/wikipedia/zh/math/f/8/e/f8e648d94a8e0c86827c1605310274c2.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\triangleleft</td>
<td><img alt="\triangleleft" src="http://upload.wikimedia.org/wikipedia/zh/math/2/d/0/2d08cb5c3db4b928ee78ebf5799272c3.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\triangleright</td>
<td><img alt="\triangleright" src="http://upload.wikimedia.org/wikipedia/zh/math/6/f/8/6f8e04d60521ae7f16ba977acc75a5be.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\infty</td>
<td><img alt="\infty" src="http://upload.wikimedia.org/wikipedia/zh/math/d/2/4/d245777abca64ece2d5d7ca0d19fddb6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\bot</td>
<td><img alt="\bot" src="http://upload.wikimedia.org/wikipedia/zh/math/2/4/6/2462ef886428ee7d949936d41281f003.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\top</td>
<td><img alt="\top" src="http://upload.wikimedia.org/wikipedia/zh/math/0/9/c/09c35e480ff978d5868d6e09f324f913.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\vdash</td>
<td><img alt="\vdash" src="http://upload.wikimedia.org/wikipedia/zh/math/b/f/7/bf73c9341a48c47c84a48dad635ff940.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\vDash</td>
<td><img alt="\vDash" src="http://upload.wikimedia.org/wikipedia/zh/math/c/1/1/c11b72dc7a3b789b717a21f90be06c47.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Vdash</td>
<td><img alt="\Vdash" src="http://upload.wikimedia.org/wikipedia/zh/math/f/a/b/fab53e7da58e75e9eb1c8b5719631e0b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\models</td>
<td><img alt="\models" src="http://upload.wikimedia.org/wikipedia/zh/math/e/7/6/e766ce0de4bbe899d7ea2ebe40b3e0ee.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\lVert</td>
<td><img alt="\lVert" src="http://upload.wikimedia.org/wikipedia/zh/math/d/8/6/d864e6c7ca350ed86ee64288afbd178a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\rVert</td>
<td><img alt="\rVert" src="http://upload.wikimedia.org/wikipedia/zh/math/f/7/8/f7898b1a0e380641f53fc4d5c2218b68.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\imath</td>
<td><img alt="\imath" src="http://upload.wikimedia.org/wikipedia/zh/math/1/b/6/1b6f7d5292201038835cfccdf34c96e3.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\hbar</td>
<td><img alt="\hbar" src="http://upload.wikimedia.org/wikipedia/zh/math/9/d/f/9dfd055ef1683b053f1b5bf9ed6dbbb4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\ell</td>
<td><img alt="\ell" src="http://upload.wikimedia.org/wikipedia/zh/math/3/3/4/334ce9eb79df1178b0380461c9eaa09e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\mho</td>
<td><img alt="\mho" src="http://upload.wikimedia.org/wikipedia/zh/math/f/f/c/ffcb76daff70c2bd4e0f4624bed32a2f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Finv</td>
<td><img alt="\Finv" src="http://upload.wikimedia.org/wikipedia/zh/math/6/a/9/6a984c8c20e99df30c065327cfce2b55.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\Re</td>
<td><img alt="\Re" src="http://upload.wikimedia.org/wikipedia/zh/math/6/e/0/6e0372ee3e41f8ed7bba429e0ccdc96e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\Im</td>
<td><img alt="\Im" src="http://upload.wikimedia.org/wikipedia/zh/math/e/f/8/ef81859e9fa4549ecefd51647be8224a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\wp</td>
<td><img alt="\wp" src="http://upload.wikimedia.org/wikipedia/zh/math/5/9/2/59234eec7b76260bbbfcf81979887b2c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\complement</td>
<td><img alt="\complement" src="http://upload.wikimedia.org/wikipedia/zh/math/8/9/f/89fb291e5e64322950296e45369d3285.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>\diamondsuit</td>
<td><img alt="\diamondsuit" src="http://upload.wikimedia.org/wikipedia/zh/math/f/b/2/fb24ec60ac1d9b437a64b2edcb5450f4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\heartsuit</td>
<td><img alt="\heartsuit" src="http://upload.wikimedia.org/wikipedia/zh/math/7/b/d/7bd6a6158c45891182ef5783234c2c5a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\clubsuit</td>
<td><img alt="\clubsuit" src="http://upload.wikimedia.org/wikipedia/zh/math/f/2/4/f243a5ff32cd1dd4a28521b225bb76b5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\spadesuit</td>
<td><img alt="\spadesuit" src="http://upload.wikimedia.org/wikipedia/zh/math/8/a/2/8a2e30359d1821a30aff595e4ff18375.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\Game</td>
<td><img alt="\Game" src="http://upload.wikimedia.org/wikipedia/zh/math/4/f/6/4f67c5c3f8e2624b0e62de0ee8d38650.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\flat</td>
<td><img alt="\flat" src="http://upload.wikimedia.org/wikipedia/zh/math/8/3/8/8380b268482c1a8d9fd36dc88e8a127a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\natural</td>
<td><img alt="\natural" src="http://upload.wikimedia.org/wikipedia/zh/math/3/1/7/3178537e3f3a2bc507823259218904ad.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>\sharp</td>
<td><img alt="\sharp" src="http://upload.wikimedia.org/wikipedia/zh/math/7/8/1/7818bf5748ed97579507cd14a1d5bb65.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **上标、下标及积分等**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>功能</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>上标</td>
<td><code>a^2</code></td>
<td><img alt="\pagecolor{White} a^2" src="http://upload.wikimedia.org/wikipedia/zh/math/f/1/d/f1d0a7eeee296f457681b906e2cdacac.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>下标</td>
<td><code>a_2</code></td>
<td><img alt="\pagecolor{White} a_2" src="http://upload.wikimedia.org/wikipedia/zh/math/8/e/2/8e2d2291a5593af94e996a65b6f726f8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">组合</td>
<td><code>a^{2+2}</code></td>
<td><img alt="\pagecolor{White} a^{2+2}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/6/8/0683bba81494fa4172f1052cec9f2eed.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>a_{i,j}</code></td>
<td><img alt="\pagecolor{White} a_{i,j}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/d/9/bd93d6a6976568f768d4ef2a91bb2151.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>结合上下标</td>
<td><code>x_2^3</code></td>
<td><img alt="\pagecolor{White} x_2^3" src="http://upload.wikimedia.org/wikipedia/zh/math/f/7/f/f7ffd853543b9b2461e72eb28f8dec3c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>前置上下标</td>
<td><code>{}_1^2\!X_3^4</code></td>
<td><img alt="\pagecolor{White} {}_1^2\!X_3^4" src="http://upload.wikimedia.org/wikipedia/zh/math/2/4/9/2491f82bb48b549a2aaf289dbb3a7bed.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><a target="_blank" href="http://zh.wikipedia.org/wiki/%E5%AF%BC%E6%95%B0" rel="nofollow" title="导数" style="color:rgb(106,57,6); text-decoration:none">导数</a><br>
（<strong>HTML</strong>）</td>
<td><code>x'</code></td>
<td><img alt="\pagecolor{White} x'" src="http://upload.wikimedia.org/wikipedia/zh/math/2/1/e/21ef9651f881246acc18a8b92368aabf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>导数<br>
（<strong>PNG</strong>）</td>
<td><code>x^\prime</code></td>
<td><img alt="\pagecolor{White} x^\prime" src="http://upload.wikimedia.org/wikipedia/zh/math/e/3/d/e3dbdd462fde1f1fb890aed48df66440.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>导数<br>
（<strong>错误</strong>）</td>
<td><code>x\prime</code></td>
<td><img alt="\pagecolor{White} x\prime" src="http://upload.wikimedia.org/wikipedia/zh/math/e/5/2/e5269181cb3851f57f684d621a9f1fca.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">导数点</td>
<td><code>\dot{x}</code></td>
<td><img alt="\pagecolor{White} \dot{x}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/3/3/733b0ff044f2e2cfdb524078740878b1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\ddot{y}</code></td>
<td><img alt="\pagecolor{White} \ddot{y}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/6/f/e6f6b45ec0ee15db8c4caa3f1fe88fdf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="4"><a target="_blank" href="http://zh.wikipedia.org/wiki/%E5%90%91%E9%87%8F" rel="nofollow" title="向量" style="color:rgb(106,57,6); text-decoration:none">向量</a></td>
<td><code>\vec{c}</code></td>
<td><img alt="\pagecolor{White} \vec{c}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/1/f/31fc19819196b91156e13edc6cb3358c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\overleftarrow{a b}</code></td>
<td><img alt="\pagecolor{White} \overleftarrow{a b}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/9/4/d948738bbfeb127b134f549321c789ff.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\overrightarrow{c d}</code></td>
<td><img alt="\pagecolor{White} \overrightarrow{c d}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/c/1/3c115f32f746e2c73d59f1a8cfbe36a2.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\widehat{e f g}</code></td>
<td><img alt="\pagecolor{White} \widehat{e f g}" src="http://upload.wikimedia.org/wikipedia/zh/math/4/c/b/4cba1e79deac23bb500a8aa203d9a111.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>上弧<br>
(注: 正确应该用 \overarc, 但在这里行不通。要用建议的语法作为解决办法)</td>
<td><code>\overset{\frown} {AB}</code></td>
<td><img alt="\pagecolor{White} \overset{\frown} {AB}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/4/0/b40456c21e931270a803c1d538d863f2.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>上划线</td>
<td><code>\overline{h i j}</code></td>
<td><img alt="\pagecolor{White} \overline{h i j}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/b/1/5b143339bea2ab5becbbb7a3bdaba555.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>下划线</td>
<td><code>\underline{k l m}</code></td>
<td><img alt="\pagecolor{White} \underline{k l m}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/4/7/147943fe9e7a222b850132ddd7882dce.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">上括号</td>
<td><code>\overbrace{1+2+\cdots+100}</code></td>
<td><img alt="\pagecolor{White} \overbrace{1+2+\cdots+100}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/9/9/e997df92fcd3679c1935cd73f5fa1a73.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} 5050 \\ \overbrace{ 1+2+\cdots+100 }\end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} 5050 \\ \overbrace{ 1+2+\cdots+100 } \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/3/c/73c0e4b49730d106b752a7c3715b0c3d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">下括号</td>
<td><code>\underbrace{a+b+\cdots+z}</code></td>
<td><img alt="\pagecolor{White} \underbrace{a+b+\cdots+z}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/7/9/d793da2820a7de9b0c645ac746da79ef.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} \underbrace{ a+b+\cdots+z } \\ 26\end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} \underbrace{ a+b+\cdots+z } \\ 26 \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/c/9/bc9dd69fffd702f4846f73579620c811.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">求和</td>
<td><code>\sum_{k=1}^N k^2</code></td>
<td><img alt="\pagecolor{White} \sum_{k=1}^N k^2" src="http://upload.wikimedia.org/wikipedia/zh/math/6/a/4/6a4791650b77862a6d6bf83f286d9f0c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} \sum_{k=1}^N k^2 \end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} \sum_{k=1}^N k^2 \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/9/c/39cf5eb70e03dff6ed87382baeca9291.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">求积</td>
<td><code>\prod_{i=1}^N x_i</code></td>
<td><img alt="\pagecolor{White} \prod_{i=1}^N x_i" src="http://upload.wikimedia.org/wikipedia/zh/math/0/9/f/09f3d0f277e7d0da504ca31e5f546988.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} \prod_{i=1}^N x_i \end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} \prod_{i=1}^N x_i \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/f/0/5f06b9aa7b4eba60f3e886bcadde28f0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">上积</td>
<td><code>\coprod_{i=1}^N x_i</code></td>
<td><img alt="\pagecolor{White} \coprod_{i=1}^N x_i" src="http://upload.wikimedia.org/wikipedia/zh/math/6/4/c/64c84feef576affcd4a7bdeb785a943c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} \coprod_{i=1}^N x_i\end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} \coprod_{i=1}^N x_i \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/5/6/e56db83ea5ba72537c2d85ed8f013276.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2"><a target="_blank" href="http://zh.wikipedia.org/wiki/%E6%9E%81%E9%99%90" rel="nofollow" title="极限" style="color:rgb(106,57,6); text-decoration:none">极限</a></td>
<td><code>\lim_{n \to \infty}x_n</code></td>
<td><img alt="\pagecolor{White} \lim_{n \to \infty}x_n" src="http://upload.wikimedia.org/wikipedia/zh/math/7/9/5/7950c79f217c0a89607656e58d4296fd.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} \lim_{n \to \infty}x_n\end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} \lim_{n \to \infty}x_n \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/7/c/e7ccfef303615810c06213be8a676484.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2"><a target="_blank" href="http://zh.wikipedia.org/wiki/%E7%A7%AF%E5%88%86" rel="nofollow" title="积分" style="color:rgb(106,57,6); text-decoration:none">积分</a></td>
<td><code>\int_{-N}^{N} e^x\, dx</code></td>
<td><img alt="\pagecolor{White} \int_{-N}^{N} e^x\, dx" src="http://upload.wikimedia.org/wikipedia/zh/math/7/4/9/7491e901a36ceb13bbbe943759b14dc8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\begin{matrix} \int_{-N}^{N} e^x\, dx\end{matrix}</code></td>
<td><img alt="\pagecolor{White} \begin{matrix} \int_{-N}^{N} e^x\, dx \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/f/6/5f6531acbd059619af09d3b52039ede5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><a target="_blank" href="http://zh.wikipedia.org/wiki/%E5%8F%8C%E9%87%8D%E7%A7%AF%E5%88%86" rel="nofollow" title="双重积分" style="color:rgb(106,57,6); text-decoration:none">双重积分</a></td>
<td><code>\iint_{D}^{W} \, dx\,dy</code></td>
<td><img alt="\pagecolor{White} \iint_{D}^{W} \, dx\,dy" src="http://upload.wikimedia.org/wikipedia/zh/math/4/4/e/44e3f99f1f29b9ee5de871e820cec5f3.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>三重积分</td>
<td><code>\iiint_{E}^{V} \, dx\,dy\,dz</code></td>
<td><img alt="\pagecolor{White} \iiint_{E}^{V} \, dx\,dy\,dz" src="http://upload.wikimedia.org/wikipedia/zh/math/8/c/0/8c050c5bd1690dd42a9f175ec124cb97.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>四重积分</td>
<td><code>\iiiint_{F}^{U} \, dx\,dy\,dz\,dt</code></td>
<td><img alt="\pagecolor{White} \iiiint_{F}^{U} \, dx\,dy\,dz\,dt" src="http://upload.wikimedia.org/wikipedia/zh/math/d/b/5/db51c71f79d301a689b3231927a0dfaa.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>闭合的<a target="_blank" href="http://zh.wikipedia.org/wiki/%E8%B7%AF%E5%BE%84%E7%A7%AF%E5%88%86" rel="nofollow" title="路径积分" style="color:rgb(106,57,6); text-decoration:none">曲线</a>、<a target="_blank" href="http://zh.wikipedia.org/wiki/%E6%9B%B2%E9%9D%A2%E7%A7%AF%E5%88%86" rel="nofollow" title="曲面积分" style="color:rgb(106,57,6); text-decoration:none">曲面积分</a></td>
<td>\oint_{C} x^3\, dx + 4y^2\, dy</td>
<td><img alt="\pagecolor{White} \oint_{C} x^3\, dx + 4y^2\, dy" src="http://upload.wikimedia.org/wikipedia/zh/math/e/5/7/e5791a184359ab19ff7e372b15ec0d1b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><a target="_blank" href="http://zh.wikipedia.org/wiki/%E4%BA%A4%E9%9B%86" rel="nofollow" title="交集" style="color:rgb(106,57,6); text-decoration:none">交集</a></td>
<td><code>\bigcap_1^{n} p</code></td>
<td><img alt="\pagecolor{White} \bigcap_1^{n} p" src="http://upload.wikimedia.org/wikipedia/zh/math/4/6/3/463d4e4bd315c0c6030354a540d85829.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><a target="_blank" href="http://zh.wikipedia.org/wiki/%E5%B9%B6%E9%9B%86" rel="nofollow" title="并集" style="color:rgb(106,57,6); text-decoration:none">并集</a></td>
<td><code>\bigcup_1^{k} p</code></td>
<td><img alt="\pagecolor{White} \bigcup_1^{k} p" src="http://upload.wikimedia.org/wikipedia/zh/math/8/0/0/80059f454f87af13803b327c202dcec1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

### **分数、矩阵和多行列式**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>功能</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<td>分数</td>
<td><code>\frac{2}{4}=0.5</code></td>
<td><img alt="\frac{2}{4}=0.5" src="http://upload.wikimedia.org/wikipedia/zh/math/4/6/d/46dc0b34e0ab4e944a437720a4431d6c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>小型分数</td>
<td><code>\tfrac{2}{4} = 0.5</code></td>
<td><img alt="\tfrac{2}{4} = 0.5" src="http://upload.wikimedia.org/wikipedia/zh/math/2/8/4/284667fc4a92790093aa59b61b3667a0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>大型分数（嵌套）</td>
<td><code>\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} =a</code></td>
<td><img alt="\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a" src="http://upload.wikimedia.org/wikipedia/zh/math/6/d/0/6d099c02b3faf73f9320656217415906.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>大型分数（不嵌套）</td>
<td><code>\dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d +\dfrac{2}{4}}} = a</code></td>
<td><img alt="\dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a" src="http://upload.wikimedia.org/wikipedia/zh/math/5/a/3/5a37ae94a95c7dd603c20cd4fbe8d9e9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><a target="_blank" href="http://zh.wikipedia.org/wiki/%E4%BA%8C%E9%A1%B9%E5%BC%8F" rel="nofollow" title="二项式" style="color:rgb(106,57,6); text-decoration:none">二项式</a>系数</td>
<td><code>\dbinom{n}{r}=\binom{n}{n-r}=C^n_r=C^n_{n-r}</code></td>
<td><img alt="\dbinom{n}{r}=\binom{n}{n-r}=C^n_r=C^n_{n-r}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/a/5/6a5373cd8c6503567a3c2a69deda71f3.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>小型<a target="_blank" href="http://zh.wikipedia.org/wiki/%E4%BA%8C%E9%A1%B9%E5%BC%8F" rel="nofollow" title="二项式" style="color:rgb(106,57,6); text-decoration:none">二项式</a>系数</td>
<td><code>\tbinom{n}{r}=\tbinom{n}{n-r}=C^n_r=C^n_{n-r}</code></td>
<td><img alt="\tbinom{n}{r}=\tbinom{n}{n-r}=C^n_r=C^n_{n-r}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/b/1/0b1188af9ee1a12bc62ca56cf83f268c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>大型<a target="_blank" href="http://zh.wikipedia.org/wiki/%E4%BA%8C%E9%A1%B9%E5%BC%8F" rel="nofollow" title="二项式" style="color:rgb(106,57,6); text-decoration:none">二项式</a>系数</td>
<td><code>\binom{n}{r}=\dbinom{n}{n-r}=C^n_r=C^n_{n-r}</code></td>
<td><img alt="\binom{n}{r}=\dbinom{n}{n-r}=C^n_r=C^n_{n-r}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/6/9/b69b21e3b047a91cd1127a498b3267f6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="7">矩阵</td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{matrix}
x &amp; y \\
z &amp; v
\end{matrix}
</pre>
</td>
<td><img alt="\begin{matrix} x &amp; y \\ z &amp; v \end{matrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/9/9/b99890966e1b997497211428f8e3419d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{vmatrix}
x &amp; y \\
z &amp; v
\end{vmatrix}
</pre>
</td>
<td><img alt="\begin{vmatrix} x &amp; y \\ z &amp; v \end{vmatrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/2/b/92b8f0e57848a80b4babd2ba93775370.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{Vmatrix}
x &amp; y \\
z &amp; v
\end{Vmatrix}
</pre>
</td>
<td><img alt="\begin{Vmatrix} x &amp; y \\ z &amp; v \end{Vmatrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/b/a/bba5bfd11057dbb202307584eed8f2dc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{bmatrix}
0      &amp; \cdots &amp; 0      \\
\vdots &amp; \ddots &amp; \vdots \\
0      &amp; \cdots &amp; 0
\end{bmatrix}
</pre>
</td>
<td><img alt="\begin{bmatrix} 0 &amp; \cdots &amp; 0 \\ \vdots &amp; \ddots &amp; \vdots \\ 0 &amp; \cdots &amp; 0\end{bmatrix} " src="http://upload.wikimedia.org/wikipedia/zh/math/8/1/a/81a12a09ac84853e3d25323b8643c630.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{Bmatrix}
x &amp; y \\
z &amp; v
\end{Bmatrix}
</pre>
</td>
<td><img alt="\begin{Bmatrix} x &amp; y \\ z &amp; v \end{Bmatrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/f/7/bf7244e2842c8a7d55892e229560d5c1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{pmatrix}
x &amp; y \\
z &amp; v
\end{pmatrix}
</pre>
</td>
<td><img alt="\begin{pmatrix} x &amp; y \\ z &amp; v \end{pmatrix}" src="http://upload.wikimedia.org/wikipedia/zh/math/4/4/4/444df88e616def4e275b4e920c7b872e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\bigl( \begin{smallmatrix}
a&amp;b\\ c&amp;d
\end{smallmatrix} \bigr)
</pre>
</td>
<td><img alt=" \bigl( \begin{smallmatrix} a&amp;b\\ c&amp;d \end{smallmatrix} \bigr) " src="http://upload.wikimedia.org/wikipedia/zh/math/c/d/4/cd49bbc188dce0f93fef57312af5a106.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>条件定义</td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">f(n) =
\begin{cases}
n/2,  &amp; \mbox{if }n\mbox{ is even} \\
3n+1, &amp; \mbox{if }n\mbox{ is odd}
\end{cases}
</pre>
</td>
<td><img alt="f(n) = \begin{cases} n/2, &amp; \mbox{if }n\mbox{ is even} \ 3n+1, &amp; \mbox{if }n\mbox{ is odd} \end{cases} " src="http://upload.wikimedia.org/wikipedia/zh/math/e/3/a/e3aebe50364cfe498fa9ca99c0036010.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="2">多行等式</td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{align}
f(x) &amp; = (m+n)^2 \\
&amp; = m^2+2mn+n^2 \\
\end{align}
</pre>
</td>
<td><img alt=" \begin{align} f(x) &amp; = (m+n)^2 \ &amp; = m^2+2mn+n^2 \ \end{align} " src="http://upload.wikimedia.org/wikipedia/zh/math/1/d/9/1d9f576360e949d08e0fac7cacbbd25c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{alignat}{2}
f(x) &amp; = (m-n)^2 \\
f(x) &amp; = (-m+n)^2 \\
&amp; = m^2-2mn+n^2 \\
\end{alignat}
</pre>
</td>
<td><img alt=" \begin{alignat}{2} f(x) &amp; = (m-n)^2 \ f(x) &amp; = (-m+n)^2 \ &amp; = m^2-2mn+n^2 \ \end{alignat} " src="http://upload.wikimedia.org/wikipedia/zh/math/1/8/d/18d4bad0865b57fc1d5b383abe2da1b0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>多行等式<small>（左对齐）</small></td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{array}{lcl}
z        &amp; = &amp; a \\
f(x,y,z) &amp; = &amp; x + y + z
\end{array}
</pre>
</td>
<td><img alt="\begin{array}{lcl} z &amp; = &amp; a \ f(x,y,z) &amp; = &amp; x + y + z \end{array}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/b/f/9bf19115bb27237fa997ca93b94ad217.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>多行等式<small>（右对齐）</small></td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{array}{lcr}
z        &amp; = &amp; a \\
f(x,y,z) &amp; = &amp; x + y + z
\end{array}
</pre>
</td>
<td><img alt="\begin{array}{lcr} z &amp; = &amp; a \ f(x,y,z) &amp; = &amp; x + y + z \end{array}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/2/a/02ae32735e1e21ba3b05984289fd2763.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>长公式换行</td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">&lt;math&gt;f(x) \,\!&lt;/math&gt;
&lt;math&gt;= \sum_{n=0}^\infty a_n x^n &lt;/math&gt;
&lt;math&gt;= a_0+a_1x+a_2x^2+\cdots&lt;/math&gt;

</pre>
</td>
<td>
<p><img alt="f(x) \,\!" src="http://upload.wikimedia.org/wikipedia/zh/math/8/d/f/8dfae20000a042d8e9047aad1d7e171e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"><img alt="= \sum_{n=0}^\infty a_n x^n " src="http://upload.wikimedia.org/wikipedia/zh/math/6/6/3/6633d51d63b35281d030755a6b0aebb1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"><img alt="= a_0 +a_1x+a_2x^2+\cdots" src="http://upload.wikimedia.org/wikipedia/zh/math/f/e/3/fe3e268382fd486e8572daf895bd4c9d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></p>
</td>
</tr>
<tr>
<td><a target="_blank" href="http://zh.wikipedia.org/wiki/%E6%96%B9%E7%A8%8B%E7%BB%84" rel="nofollow" title="方程组" style="color:rgb(106,57,6); text-decoration:none">方程组</a></td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{cases}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{cases}
</pre>
</td>
<td><img alt="\begin{cases} 3x + 5y + z \\ 7x - 2y + 4z \\ -6x + 3y + 2z \end{cases}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/3/4/6349be04b3562fc215c7a4e130422a96.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>数组</td>
<td>
<pre style="white-space:pre-wrap; word-wrap:break-word">\begin{array}{|c|c||c|} a &amp; b &amp; S \\
\hline
0&amp;0&amp;1\\
0&amp;1&amp;1\\
1&amp;0&amp;1\\
1&amp;1&amp;0\\
\end{array}
</pre>
</td>
<td><img alt=" \begin{array}{|c|c||c|} a &amp; b &amp; S \ \hline 0&amp;0&amp;1\ 0&amp;1&amp;1\ 1&amp;0&amp;1\ 1&amp;1&amp;0\ \end{array} " src="http://upload.wikimedia.org/wikipedia/zh/math/9/1/5/9151e94ef2bb52c18176dbe4c11921ed.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

## **字体**
### **希腊字母**
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
斜体小写希腊字母一般用于在方程中显示变量。</p>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th colspan="4">
<center>正体希腊字母</center>
</th>
</tr>
<tr>
<th>特征</th>
<th>语法</th>
<th>效果</th>
<th>注释/外部链接</th>
</tr>
<tr>
<th rowspan="3">
<center>大写字母</center>
</th>
<td><code>\Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta\Theta</code></td>
<td><img alt="\Alpha\Beta\Gamma\Delta\Epsilon\Zeta\Eta\Theta\!" src="http://upload.wikimedia.org/wikipedia/zh/math/a/7/a/a7a8e6bbde24e99f9dab00c840f9483d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<th>
<center><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%91" rel="nofollow" title="Α" style="color:rgb(106,57,6); text-decoration:none">Α</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%92" rel="nofollow" title="Β" style="color:rgb(106,57,6); text-decoration:none">Β</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%93" rel="nofollow" title="Γ" style="color:rgb(106,57,6); text-decoration:none">Γ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%94" rel="nofollow" title="Δ" style="color:rgb(106,57,6); text-decoration:none">Δ</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%95" rel="nofollow" title="Ε" style="color:rgb(106,57,6); text-decoration:none">Ε</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%96" rel="nofollow" title="Ζ" style="color:rgb(106,57,6); text-decoration:none">Ζ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%97" rel="nofollow" title="Η" style="color:rgb(106,57,6); text-decoration:none">Η</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%98" rel="nofollow" title="Θ" style="color:rgb(106,57,6); text-decoration:none">Θ</a></center>
</th>
</tr>
<tr>
<td><code>\Iota \Kappa \Lambda \Mu \Nu \Xi \Omicron \Pi</code></td>
<td><img alt="\Iota\Kappa\Lambda\Mu\Nu\Xi\Omicron\Pi\!" src="http://upload.wikimedia.org/wikipedia/zh/math/0/e/0/0e022245aac65d3fe5eaf14065761066.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<th>
<center><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%99" rel="nofollow" title="Ι" style="color:rgb(106,57,6); text-decoration:none">Ι</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%9A" rel="nofollow" title="Κ" style="color:rgb(106,57,6); text-decoration:none">Κ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%9B" rel="nofollow" title="Λ" style="color:rgb(106,57,6); text-decoration:none">Λ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%9C" rel="nofollow" title="Μ" style="color:rgb(106,57,6); text-decoration:none">Μ</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%9D" rel="nofollow" title="Ν" style="color:rgb(106,57,6); text-decoration:none">Ν</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%9E" rel="nofollow" title="Ξ" style="color:rgb(106,57,6); text-decoration:none">Ξ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%9F" rel="nofollow" title="Ο" style="color:rgb(106,57,6); text-decoration:none">Ο</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A0" rel="nofollow" title="Π" style="color:rgb(106,57,6); text-decoration:none">Π</a></center>
</th>
</tr>
<tr>
<td><code>\Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi\Omega</code></td>
<td><img alt="\Rho\Sigma\Tau\Upsilon\Phi\Chi\Psi\Omega\!" src="http://upload.wikimedia.org/wikipedia/zh/math/e/f/c/efc3244ff48644b6134ee45563b49b45.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<th>
<center><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A1" rel="nofollow" title="Ρ" style="color:rgb(106,57,6); text-decoration:none">Ρ</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A3" rel="nofollow" title="Σ" style="color:rgb(106,57,6); text-decoration:none">Σ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A4" rel="nofollow" title="Τ" style="color:rgb(106,57,6); text-decoration:none">Τ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A5" rel="nofollow" title="Υ" style="color:rgb(106,57,6); text-decoration:none">Υ</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A6" rel="nofollow" title="Φ" style="color:rgb(106,57,6); text-decoration:none">Φ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A7" rel="nofollow" title="Χ" style="color:rgb(106,57,6); text-decoration:none">Χ</a>&nbsp;<a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A8" rel="nofollow" title="Ψ" style="color:rgb(106,57,6); text-decoration:none">Ψ</a><a target="_blank" href="http://zh.wikipedia.org/wiki/%CE%A9" rel="nofollow" title="Ω" style="color:rgb(106,57,6); text-decoration:none">Ω</a></center>
</th>
</tr>
<tr>
<th rowspan="3">
<center>小写字母</center>
</th>
<td><code>\alpha \beta \gamma \delta \epsilon \zeta \eta\theta</code></td>
<td><img alt="\alpha\beta\gamma\delta\epsilon\zeta\eta\theta\!" src="http://upload.wikimedia.org/wikipedia/zh/math/9/f/e/9fef94989f0aefed4c953823bd945e89.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\iota \kappa\varkappa \lambda \mu \nu \xi \omicron\pi</code></td>
<td><img alt="\iota\kappa\varkappa\lambda\mu\nu\xi\omicron\pi\!" src="http://upload.wikimedia.org/wikipedia/zh/math/2/1/f/21fef848efb59d5bf6168bfb9a8755ab.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\rho \sigma \tau \upsilon \phi \chi \psi\omega</code></td>
<td><img alt="\rho\sigma\tau\upsilon\phi\chi\psi\omega\!" src="http://upload.wikimedia.org/wikipedia/zh/math/1/1/3/1136b70309d44ecdbacbba66bf42ceb8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<th rowspan="7">
<center>异体字母</center>
</th>
<td><code>\Epsilon\epsilon\varepsilon</code></td>
<td><img alt="\Epsilon\epsilon\varepsilon" src="http://upload.wikimedia.org/wikipedia/zh/math/9/9/c/99c715d6c6eb8fb0c7788b0496c18fcf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\Theta\theta\vartheta</code></td>
<td><img alt="\Theta\theta\vartheta" src="http://upload.wikimedia.org/wikipedia/zh/math/c/8/5/c85d2107efa86dfe8e8954e8104941c6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\Kappa\kappa\varkappa</code></td>
<td><img alt="\Kappa\kappa\varkappa" src="http://upload.wikimedia.org/wikipedia/zh/math/7/b/8/7b8b29c367a46e3d1403cb76cbbbf028.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\Pi\pi\varpi</code></td>
<td><img alt="\Pi\pi\varpi" src="http://upload.wikimedia.org/wikipedia/zh/math/2/1/5/215d2b61e8b6fa92a374ea7f6fd0adf6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\Rho\rho\varrho</code></td>
<td><img alt="\Rho\rho\varrho" src="http://upload.wikimedia.org/wikipedia/zh/math/3/1/a/31accc86698f4bc68e6a7fc57d5aba5e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\Sigma\sigma\varsigma</code></td>
<td><img alt="\Sigma\sigma\varsigma" src="http://upload.wikimedia.org/wikipedia/zh/math/6/3/3/633e6a1a75704bfc8ccb0ad3aafa22d1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><code>\Phi\phi\varphi</code></td>
<td><img alt="\Phi\phi\varphi\," src="http://upload.wikimedia.org/wikipedia/zh/math/0/f/f/0ff9115861d9a54f1529074db5fef99f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td>&nbsp;</td>
</tr>
<tr>
<th>
<center>已停用字母</center>
</th>
<td><code>\digamma</code></td>
<td><img alt="\digamma" src="http://upload.wikimedia.org/wikipedia/zh/math/2/f/0/2f057b6e514c8ca2d9cf9a3e549f8865.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<th>
<center><a target="_blank" href="http://zh.wikipedia.org/wiki/%CF%9C" rel="nofollow" title="Ϝ" style="color:rgb(106,57,6); text-decoration:none">Ϝ</a><sup><a target="_blank" href="http://zh.wikipedia.org/wiki/Help:MATH#cite_note-waw-0" rel="nofollow" style="color:rgb(106,57,6); text-decoration:none">[1]</a></sup></center>
</th>
</tr>
</tbody>
</table></div>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th colspan="3">
<center>粗体希腊字母</center>
</th>
</tr>
<tr>
<th>特征</th>
<th>语法</th>
<th>效果</th>
</tr>
<tr>
<th rowspan="3">
<center>大写字母</center>
</th>
<td><code>\boldsymbol{\Alpha \Beta \Gamma \Delta \Epsilon \Zeta\Eta \Theta}</code></td>
<td><img alt="\boldsymbol{\Alpha\Beta\Gamma\Delta\Epsilon\Zeta\Eta\Theta}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/4/f/94fb9b3acc279b36e71cffa687bed874.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Iota \Kappa \Lambda \Mu \Nu \Xi \Omicron\Pi}</code></td>
<td><img alt="\boldsymbol{\Iota\Kappa\Lambda\Mu\Nu\Xi\Omicron\Pi}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/5/f/85f3fd2f163b3adc58786af782b08de7.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi\Omega}</code></td>
<td><img alt="\boldsymbol{\Rho\Sigma\Tau\Upsilon\Phi\Chi\Psi\Omega}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/0/f/c0f2474ad244a26ea4e6151bd8bd32ea.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<th rowspan="3">
<center>小写字母</center>
</th>
<td><code>\boldsymbol{\alpha \beta \gamma \delta \epsilon \zeta\eta \theta}</code></td>
<td><img alt="\boldsymbol{\alpha\beta\gamma\delta\epsilon\zeta\eta\theta}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/1/7/c17de9504191bfa32a07aeb91ddb4951.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\iota \kappa \lambda \mu \nu \xi \omicron\pi}</code></td>
<td><img alt="\boldsymbol{\iota\kappa\lambda\mu\nu\xi\omicron\pi}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/9/2/7928383f5c482c3f54b174a8587ef072.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\rho \sigma \tau \upsilon \phi \chi \psi\omega}</code></td>
<td><img alt="\boldsymbol{\rho\sigma\tau\upsilon\phi\chi\psi\omega}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/3/5/c35ae2ba2495c03800061cce1a891ac9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<th rowspan="7">
<center>异体字母</center>
</th>
<td><code>\boldsymbol{\Epsilon\epsilon\varepsilon}</code></td>
<td><img alt="\boldsymbol{\Epsilon\epsilon\varepsilon}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/3/9/c39ce84cdcacc3e61acb968df349f8c2.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Theta\theta\vartheta}</code></td>
<td><img alt="\boldsymbol{\Theta\theta\vartheta}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/d/3/ad38436580b9494806467c8840c3bece.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Kappa\kappa\varkappa}</code></td>
<td><img alt="\boldsymbol{\Kappa\kappa\varkappa}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/a/9/ca9ff8676cb9fda962e4f1ac89c6a3e6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Pi\pi\varpi}</code></td>
<td><img alt="\boldsymbol{\Pi\pi\varpi}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/d/6/ad6b8d8282bfeef3c52a351bb71b218f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Rho\rho\varrho}</code></td>
<td><img alt="\boldsymbol{\Rho\rho\varrho}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/2/6/026b48b451f2f85218243a435c0e62c8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Sigma\sigma\varsigma}</code></td>
<td><img alt="\boldsymbol{\Sigma\sigma\varsigma}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/9/3/99382bedcd762954e10b7bd59da12101.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><code>\boldsymbol{\Phi\phi\varphi}</code></td>
<td><img alt="\boldsymbol{\Phi\phi\varphi}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/4/8/7480345aa28c6c4f01d80ab7f67996a1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<th>
<center>已停用字母</center>
</th>
<td><code>\boldsymbol{\digamma}</code></td>
<td>&nbsp;</td>
</tr>
</tbody>
</table></div>

### **黑板粗体**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\mathbb{</strong><em>ABCDEFGHIJKLMNOPQRSTUVWX<wbr>YZ</em><strong>}</strong></code></dd><dt>效果</dt><dd><img alt="\pagecolor{White}\mathbb{ABCDEFGHIJKLMNOPQRSTUVWXYZ}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/e/4/ce44c3481a2b5d78785b0c920f5a4614.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
黑板粗体（<a target="_blank" href="http://en.wikipedia.org/wiki/Blackboard_bold" rel="nofollow" title="en:Blackboard bold" style="color:rgb(106,57,6); text-decoration:none">Blackboardbold</a>）一般用于表示数学和物理学中的向量或集合的符号。 备注：</p>
<ol style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<li><img alt="\{ \," src="http://upload.wikimedia.org/wikipedia/zh/math/6/9/b/69b3f95ebb53ab73dc89a39639392f86.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%">花括号<img alt="\} \," src="http://upload.wikimedia.org/wikipedia/zh/math/b/7/5/b752132764734448b12a5a3dd2cda51c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%">中只有使用大写拉丁字母才能正常显示，使用小写字母或数字会得到其他符号。</li></ol>

### **正粗体**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\mathbf{</strong><em>012…abc…ABC…</em><strong>}</strong></code></dd><dt>效果</dt><dd><img alt="\pagecolor{White}\mathbf{0 \ 1 \ 2 \ 3 \ 4 \ 5 \ 6 \ 7 \ 8 \ 9}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/7/6/77638faf12d57998f2e9b73e943de27c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White}\mathbf{a \ b \ c \ d \ e \ f \ g \ h \ i \ j \ k \ l \ m \ n \ o \ p \ q \ r \ s \ t \ u \ v \ w \ x \ y \ z}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/6/6/1662b633eb414e7b094e8f34e4108f3a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White}\mathbf{A \ B \ C \ D \ E \ F \ G \ H \ I \ J \ K \ L \ M \ N \ O \ P \ Q \ R \ S \ T \ U \ V \ W \ X \ Y \ Z}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/0/580fd155c65a7dc6f92cfa4dfb973ed5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dt>备注</dt><dd>花括号{}内只能使用拉丁字母和数字，不能使用希腊字母如\alpha等。斜粗体</dd></dl>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\boldsymbol{</strong><em>012…abc…ABC…\alpha \beta\gamma…</em><strong>}</strong></code></dd><dt>效果</dt><dd><img alt="\pagecolor{White}\boldsymbol{0 \ 1 \ 2 \ 3 \ 4 \ 5 \ 6 \ 7 \ 8 \ 9}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/9/0/a90278c14f5690a74ed5a6a8302c9082.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White}\boldsymbol{a \ b \ c \ d \ e \ f \ g \ h \ i \ j \ k \ l \ m \ n \ o \ p \ q \ r \ s \ t \ u \ v \ w \ x \ y \ z}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/d/e/aded24ff1434a136f279a7bef76514e7.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White}\boldsymbol{A \ B \ C \ D \ E \ F \ G \ H \ I \ J \ K \ L \ M \ N \ O \ P \ Q \ R \ S \ T \ U \ V \ W \ X \ Y \ Z}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/a/5/6a53c91894a6ffb4be339e91549a8423.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White}\boldsymbol{\alpha \ \beta \ \gamma \ \delta \ \epsilon \ \zeta \ \eta \ \theta \ \iota \ \kappa \ \lambda \ \mu \ \nu \ \xi \ o \ \pi \ \rho \ \sigma \ \tau \ \upsilon \ \phi \ \chi \ \psi \ \omega}" src="http://upload.wikimedia.org/wikipedia/zh/math/2/5/b/25ba644b7c4d6ea15e453246149a5fc7.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dt>备注</dt><dd>使用<code>\boldsymbol{}</code>可以加粗所有合法的符号。</dd></dl>

### **斜体数字**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\mathit{</strong><em>0123456789</em><strong>}</strong></code></dd><dt>效果</dt><dd><img alt="\mathit{0123456789}\!" src="http://upload.wikimedia.org/wikipedia/zh/math/9/6/8/96846c8042557a593245c9adbfadcf67.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>

### **罗马体**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\mathrm{</strong><em>012…abc…ABC…</em><strong>}</strong>或<strong>\mbox{}</strong>或<strong>\operatorname{}</strong></code></dd><dt>效果</dt><dd><img alt="\mathrm{0123456789}\ " src="http://upload.wikimedia.org/wikipedia/zh/math/1/5/4/15472007a8874b45b1dc0b446928e792.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\mathrm{ABCDEFGHIJKLMNOPQRSTUVWXYZ}\ " src="http://upload.wikimedia.org/wikipedia/zh/math/3/6/a/36ab31702c21e576eeb46bcb3af9492d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\mathrm{abcdefghijklmnopqrstuvwxyz}\ " src="http://upload.wikimedia.org/wikipedia/zh/math/6/2/5/6253a68230884ac36ac5705cc943cf35.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dt>备注</dt><dd>罗马体可以使用数字和<a target="_blank" href="http://zh.wikipedia.org/wiki/%E6%8B%89%E4%B8%81%E5%AD%97%E6%AF%8D" rel="nofollow" title="拉丁字母" style="color:rgb(106,57,6); text-decoration:none">拉丁字母</a>。</dd></dl>

### **哥特体**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\mathfrak{</strong><em>012…abc…ABC…</em><strong>}</strong></code></dd><dt>效果</dt><dd><img alt="\pagecolor{White} \mathfrak{0 \ 1 \ 2 \ 3 \ 4 \ 5 \ 6 \ 7 \ 8 \ 9}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/9/7/8978258d44abd5fa142106d7d0d5cfdb.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White} \mathfrak{a \ b \ c \ d \ e \ f \ g \ h \ i \ j \ k \ l \ m \ n \ o \ p \ q \ r \ s \ t \ u \ v \ w \ x \ y \ z}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/3/0/0304e047f276ed327b84d340e393b7d4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dd><img alt="\pagecolor{White} \mathfrak{A \ B \ C \ D \ E \ F \ G \ H \ I \ J \ K \ L \ M \ N \ O \ P \ Q \ R \ S \ T \ U \ V \ W \ X \ Y \ Z}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/a/9/ea949c322ae53aaf0a0de51dc465cf3f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dt>备注</dt><dd>哥特体可以使用数字和拉丁字母。</dd></dl>

### **手写体**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code><strong>\mathcal{</strong><em>ABC…</em><strong>}</strong></code></dd><dt>效果</dt><dd><img alt="\mathcal{ABCDEFGHIJKLMNOPSTUVWXYZ}" src="http://upload.wikimedia.org/wikipedia/zh/math/4/a/8/4a8cadf2764770249d0cc7bb1d8c5b94.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd><dt>备注</dt><dd>手写体仅对大写拉丁字母有效。</dd></dl>

### **希伯来字母**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt><dd><code>\aleph\beth\gimel\daleth</code></dd><dt>效果</dt><dd><img alt="\aleph\beth\gimel\daleth" src="http://upload.wikimedia.org/wikipedia/zh/math/8/b/9/8b995d7f3c72ab2bfffec5fe0bdb5df1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>

## **括号**
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>功能</th>
<th>语法</th>
<th>显示</th>
</tr>
<tr>
<td>不好看</td>
<td>( \frac{1}{2} )</td>
<td><img alt="( \frac{1}{2} )" src="http://upload.wikimedia.org/wikipedia/zh/math/4/0/a/40ad9d3d1fc9a61e16d22d7e3f854fec.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>好看了</td>
<td>\left( \frac{1}{2} \right)</td>
<td><img alt="\left ( \frac{1}{2} \right )" src="http://upload.wikimedia.org/wikipedia/zh/math/2/8/b/28bcd5b82ce0e92b25e8a0b4bd5be215.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
您可以使用&nbsp;<code>\left</code>&nbsp;和&nbsp;<code>\right</code>&nbsp;来显示不同的括号：</p>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>功能</th>
<th>语法</th>
<th>显示</th>
</tr>
<tr>
<td>圆括号，小括号</td>
<td>\left<strong>(</strong>&nbsp;\frac{a}{b} \right<strong>)</strong></td>
<td><img alt="\left( \frac{a}{b} \right)" src="http://upload.wikimedia.org/wikipedia/zh/math/2/9/0/2905969500b40b2f2c7078206e7e0e81.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>方括号，中括号</td>
<td>\left<strong>[</strong>&nbsp;\frac{a}{b} \right<strong>]</strong></td>
<td><img alt="\left[ \frac{a}{b} \right]" src="http://upload.wikimedia.org/wikipedia/zh/math/8/5/8/8585c96f355f7e301fd5143bea32efaf.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>花括号，大括号</td>
<td>\left<strong>\{</strong>&nbsp;\frac{a}{b} \right<strong>\}</strong></td>
<td><img alt="\left\{ \frac{a}{b} \right\}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/4/d/c4d4af6bab9a0e6532dddd50e7d27158.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>角括号</td>
<td>\left&nbsp;<strong>\langle</strong>&nbsp;\frac{a}{b} \right&nbsp;<strong>\rangle</strong></td>
<td><img alt="\left\langle \frac{a}{b} \right \rangle" src="http://upload.wikimedia.org/wikipedia/zh/math/d/0/6/d06e733ce705ed26a7e048dbd2945371.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>单竖线，绝对值</td>
<td>\left<strong>|</strong>&nbsp;\frac{a}{b} \right<strong>|</strong></td>
<td><img alt="\left| \frac{a}{b} \right|" src="http://upload.wikimedia.org/wikipedia/zh/math/4/0/d/40d6c8253b08e8801a01b3f6e5069a62.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>双竖线，范</td>
<td>\left&nbsp;<strong>\|</strong>&nbsp;\frac{a}{b} \right&nbsp;<strong>\|</strong></td>
<td><img alt="\left \| \frac{a}{b} \right \|" src="http://upload.wikimedia.org/wikipedia/zh/math/f/3/0/f30a5c412d1e4b4e7c6195ff5d47e947.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>取整函数<br>
（Floor function）</td>
<td>\left&nbsp;<strong>\lfloor</strong>&nbsp;\frac{a}{b} \right&nbsp;<strong>\rfloor</strong></td>
<td><img alt="\left \lfloor \frac{a}{b} \right \rfloor" src="http://upload.wikimedia.org/wikipedia/zh/math/c/0/7/c07e1fc7c0150828e55da4efe37e8a3f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>取顶函数<br>
（Ceiling function)</td>
<td>\left&nbsp;<strong>\lceil</strong>&nbsp;\frac{c}{d} \right&nbsp;<strong>\rceil</strong></td>
<td><img alt="\left \lceil \frac{c}{d} \right \rceil" src="http://upload.wikimedia.org/wikipedia/zh/math/8/6/8/868c1e52c339e01204aa1a77d44e3c71.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>斜线与反斜线</td>
<td>\left&nbsp;<strong>/</strong>&nbsp;\frac{a}{b} \right&nbsp;<strong>\backslash</strong></td>
<td><img alt="\left / \frac{a}{b} \right \backslash " src="http://upload.wikimedia.org/wikipedia/zh/math/2/f/3/2f3c5907c0a4fc4fda69eb71890ce952.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td rowspan="3">上下箭头</td>
<td>\left&nbsp;<strong>\uparrow</strong>&nbsp;\frac{a}{b} \right&nbsp;<strong>\downarrow</strong></td>
<td><img alt="\pagecolor{White}\left \uparrow \frac{a}{b} \right \downarrow " src="http://upload.wikimedia.org/wikipedia/zh/math/b/f/8/bf8dd6b753cb6aeb801ea23de51ad5bc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\left&nbsp;<strong>\Uparrow</strong>&nbsp;\frac{a}{b} \right&nbsp;<strong>\Downarrow</strong></td>
<td><img alt="\pagecolor{White}\left \Uparrow \frac{a}{b} \right \Downarrow " src="http://upload.wikimedia.org/wikipedia/zh/math/3/d/e/3de7822465115ade10b47634c22b6b7d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>\left&nbsp;<strong>\updownarrow</strong>&nbsp;\frac{a}{b} \right<strong>\Updownarrow</strong></td>
<td><img alt="\pagecolor{White}\left \updownarrow \frac{a}{b} \right \Updownarrow" src="http://upload.wikimedia.org/wikipedia/zh/math/0/6/b/06b15cbba4d935fe84a1a503603e4eb0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>混合括号</td>
<td>\left [ 0,1 \right )<br>
\left \langle \psi \right |</td>
<td><img alt="\left [ 0,1 \right )" src="http://upload.wikimedia.org/wikipedia/zh/math/a/3/8/a38771eae1778d0e214f6596a8dc1337.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"><br>
<img alt="\left \langle \psi \right |" src="http://upload.wikimedia.org/wikipedia/zh/math/d/a/2/da25fc177fd4c53a2c3399c25685dd4c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>单左括号</td>
<td>\left \{ \frac{a}{b}&nbsp;<strong>\right .</strong></td>
<td><img alt="\left \{ \frac{a}{b} \right ." src="http://upload.wikimedia.org/wikipedia/zh/math/c/e/d/ced2a2fb558fe49fa56018b9f8fd69d5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>单右括号</td>
<td><strong>\left .</strong>&nbsp;\frac{a}{b} \right \}</td>
<td><img alt="\left . \frac{a}{b} \right \}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/a/c/9ac9b3c6d21c56f5b2b474b0ea1c4b8a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
备注：</p>
<ul style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<li>可以使用&nbsp;<code>\big, \Big, \bigg, \Bigg</code>&nbsp;控制括号的大小，比如代码</li></ul>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dd><code><strong>\Bigg</strong>&nbsp;(&nbsp;<strong>\bigg</strong>&nbsp;[&nbsp;<strong>\Big</strong>&nbsp;\{<strong>\big</strong>\langle \left | \| \frac{a}{b} \| \right |&nbsp;<strong>\big</strong>&nbsp;\rangle<strong>\Big</strong>\}<strong>\bigg</strong>&nbsp;]&nbsp;<strong>\Bigg</strong>&nbsp;)</code></dd></dl>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
　显示︰<br>
</p>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dd><img alt="\pagecolor{White}\Bigg ( \bigg [ \Big \{ \big \langle \left | \| x \| \right | \big \rangle \Big \} \bigg ] \Bigg )" src="http://upload.wikimedia.org/wikipedia/zh/math/9/0/9/90905682eff0186bd5d70a201f4e4538.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>

## **空格**
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
注意<span style="font-family:cmr10,serif"><span lang="en" style="font-family:serif">T</span><span style="vertical-align:-0.5ex; margin-left:-0.1667em; margin-right:-0.125em; text-transform:uppercase"><span lang="en" style="font-family:serif">E</span></span><span lang="en" style="font-family:serif">X</span></span>能够自动处理大多数的空格，但是您有时候需要自己来控制。</p>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<tbody>
<tr>
<th>功能</th>
<th>语法</th>
<th>显示</th>
<th>宽度</th>
</tr>
<tr>
<td>2个quad空格</td>
<td><code>\alpha\qquad\beta</code></td>
<td><img alt="\alpha\qquad\beta" src="http://upload.wikimedia.org/wikipedia/zh/math/4/3/b/43ba5910626e8cdd1e7c87f87457bc68.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="2m\ " src="http://upload.wikimedia.org/wikipedia/zh/math/d/8/a/d8a3700be4ced531e5618e8bebfece25.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>quad空格</td>
<td><code>\alpha\quad\beta</code></td>
<td><img alt="\alpha\quad\beta" src="http://upload.wikimedia.org/wikipedia/zh/math/b/d/b/bdbaa56ab92dbec191da654efcf15f31.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="m\ " src="http://upload.wikimedia.org/wikipedia/zh/math/d/4/8/d482d61667a2a8f3a40b25f2626b6d16.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>大空格</td>
<td><code>\alpha\ \beta</code></td>
<td><img alt="\alpha\ \beta" src="http://upload.wikimedia.org/wikipedia/zh/math/8/c/c/8cc37fcc9fc3729b33095484307b65e9.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\frac{m}{3}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/b/d/8bd0331723b650fa4e57c0c97ea74bdb.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>中等空格</td>
<td><code>\alpha\;\beta</code></td>
<td><img alt="\alpha\;\beta" src="http://upload.wikimedia.org/wikipedia/zh/math/1/9/a/19aad8cbec4cda349710592cddcbae8a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\frac{2m}{7}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/8/6/d86c7e706d3844153628c5344a0d43c3.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>小空格</td>
<td><code>\alpha\,\beta</code></td>
<td><img alt="\alpha\,\beta" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/0/580e640ac8bd1b0b421e62a48f9d4815.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\frac{m}{6}" src="http://upload.wikimedia.org/wikipedia/zh/math/2/b/2/2b25f9317e1ebccefa69c899bb87f655.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>没有空格</td>
<td><code>\alpha\beta</code></td>
<td><img alt="\alpha\beta\ " src="http://upload.wikimedia.org/wikipedia/zh/math/c/7/6/c761464c4ea7b0a18e7bd830bc80fc62.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="0\ " src="http://upload.wikimedia.org/wikipedia/zh/math/5/7/1/571e19a3fb35a2f712cd608e89b85dc5.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td>紧贴</td>
<td><code>\alpha\!\beta</code></td>
<td><img alt="\alpha\!\beta" src="http://upload.wikimedia.org/wikipedia/zh/math/6/d/3/6d331458bfd8a10d0639514187a1eb42.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="-\frac{m}{6}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/a/4/1a40f481cfa743830b2c80b87a4acccc.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>

## **颜色**
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>语法</dt></dl>
<ul style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<li>字体颜色︰<code>{\color{色调}表达式}</code><br>
</li><li>背景颜色︰<code>{\pagecolor{色调}表达式}</code></li></ul>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>支援色调表</dt></dl>
<div class="table-box"><table style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px; text-align:left">
<caption>Colors supported</caption>
<tbody>
<tr>
<td><img alt="\color{Apricot}\text{Apricot}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/8/9/b8948aeb7bdca5bd4e18d613ac6c5696.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Aquamarine}\text{Aquamarine}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/c/4/fc435c38d6cd34147f1b0562b0e580c0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Bittersweet}\text{Bittersweet}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/6/7/d67b10dd93c2300ee8d13b5099078d1b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Black}\text{Black}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/6/4/364fc160f6c30914ad3d70a6bb551dc6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Blue}\text{Blue}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/f/7/5f795126f5d16b97c60578f01b368cd6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{BlueGreen}\text{BlueGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/0/2/302ea2ab02b2998679c1f973dfb17395.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{BlueViolet}\text{BlueViolet}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/7/d/f7d3a6b44f64ec4d9b289bf8ac436d92.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{BrickRed}\text{BrickRed}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/2/f/a2f94714d1809cb3f71016db0e8c2315.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Brown}\text{Brown}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/9/c/99cfd151aa2998fb6b309c8c50393c32.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{BurntOrange}\text{BurntOrange}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/e/3/3e3b04676ace992e28aaa5608455a289.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{CadetBlue}\text{CadetBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/d/3/fd392c22a7bb76e6203788f0a5e6584b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{CarnationPink}\text{CarnationPink}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/0/7/6079cf2eacc794bf3e99bc9fc233e2d0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Cerulean}\text{Cerulean}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/7/5/9759c3640f8f5a2cfa5cfa5c4bc64e2f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{CornflowerBlue}\text{CornflowerBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/7/2/072ea0cddb81b6996a86c5c60042fc8c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Cyan}\text{Cyan}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/2/1/321ecf031772dbe95758cab0dfaa6f27.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Dandelion}\text{Dandelion}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/8/6/78686b75a31528404d2e9b365f892142.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{DarkOrchid}\text{DarkOrchid}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/9/b/19bc495f720e6bb920eed9545880e383.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Emerald}\text{Emerald}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/4/3/b4310eecc8d70893a71a728574dc9f0f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{ForestGreen}\text{ForestGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/8/9/b89859eb7faadeb40830600590478e6e.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Fuchsia}\text{Fuchsia}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/0/7/3073bfb913846b8b74d221b3de291348.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Goldenrod}\text{Goldenrod}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/f/6/af66a8061a03abb89bc4d205503d437f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Gray}\text{Gray}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/e/5/1e5478f23b28143107d25266b55ef78a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Green}\text{Green}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/4/7/9474b1edd45b5aefe4533543fe85bbbd.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="background-color:gray"><img alt="\pagecolor{Gray}\color{GreenYellow}\text{GreenYellow}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/f/1/8f10b1195e9646f9ca5fbf15001a5b12.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{JungleGreen}\text{JungleGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/7/2/f72158890930502ffd7dae256812f7e4.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Lavender}\text{Lavender}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/2/f/f2fa7339ac0b50f73409f1e05eb77800.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{LimeGreen}\text{LimeGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/c/4/c/c4c5d14dea2c682d5f4148eab87e332f.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Magenta}\text{Magenta}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/9/b/d9bfd6c63b5b8c21f53e52a74a75eb97.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Mahogany}\text{Mahogany}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/b/b/dbb2ef205ba8d4d3586b1b9785c54c25.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Maroon}\text{Maroon}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/6/5861b59a922bda9d96cf03cb8a184a8a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Melon}\text{Melon}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/9/b/e9b605ab8c6a1135ac9bb24e540e645b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{MidnightBlue}\text{MidnightBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/3/c/1/3c196c0de1592080c250b05208cb29c1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Mulberry}\text{Mulberry}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/8/f/78fe49c7ffa31d0309ecad4e17c8533b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{NavyBlue}\text{NavyBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/b/5/7/b57ac6d698f2a553d1de298b8ae86f55.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{OliveGreen}\text{OliveGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/f/f/1ff90d0c4e6d6901579206062701309a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Orange}\text{Orange}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/d/d/1dd73f756801b262f01f87912b369339.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{OrangeRed}\text{OrangeRed}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/d/f/6df4aca479f5fa8acae9c21141636557.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Orchid}\text{Orchid}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/0/3/e03e079ac7c0138cc85bb20894e42c7d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Peach}\text{Peach}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/6/a/16a4afaaa911b78f102f2e088c596715.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Periwinkle}\text{Periwinkle}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/0/4/104bee7d6969d0403571f7aa65390384.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{PineGreen}\text{PineGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/8/2/5821d738015d4bae29a90be43c9dc760.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Plum}\text{Plum}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/e/3/de3328ac78da89a5e86e1917ec8fb87b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{ProcessBlue}\text{ProcessBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/2/0/e20ab4232d3130d086b8de76eee6b53c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Purple}\text{Purple}" src="http://upload.wikimedia.org/wikipedia/zh/math/f/e/f/fefd1c1377e3d29213e81e866583adad.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{RawSienna}\text{RawSienna}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/4/5/745d3d1a6a79b318a497e6fbcb57dc02.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Red}\text{Red}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/e/2/9e2052c4c91b5216205fe642a06c5ac1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{RedOrange}\text{RedOrange}" src="http://upload.wikimedia.org/wikipedia/zh/math/2/a/0/2a026699e64707b449d7c3811d752725.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{RedViolet}\text{RedViolet}" src="http://upload.wikimedia.org/wikipedia/zh/math/2/a/c/2ac9ad9fbd882591f7971ff477880fe6.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Rhodamine}\text{Rhodamine}" src="http://upload.wikimedia.org/wikipedia/zh/math/2/7/d/27d615add22f24e5689271903afd2ea8.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{RoyalBlue}\text{RoyalBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/e/2/6e26c2a826a4d55150b804f2e71444af.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{RoyalPurple}\text{RoyalPurple}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/d/4/dd4a6069922baf4c048592b1bccef491.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{RubineRed}\text{RubineRed}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/7/1/771e441e86b10ef3db7b7cb90d9570d1.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Salmon}\text{Salmon}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/2/0/1204c3c0547f50b71bda5357deba7948.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{SeaGreen}\text{SeaGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/8/9/e897b90beb4e669c01a63c3d2ac2d954.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Sepia}\text{Sepia}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/3/b/e3b0037782599bf00cec26b758627e4b.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{SkyBlue}\text{SkyBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/3/b/03bc1de1505a991d0f8c2db1a9211740.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td style="background-color:gray"><img alt="\pagecolor{Gray}\color{SpringGreen}\text{SpringGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/d/7/4/d747177fd9554cc703043bf3dfeaad7d.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Tan}\text{Tan}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/9/7/6975e0f90106c5e304d39dfebc6ad1d0.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{TealBlue}\text{TealBlue}" src="http://upload.wikimedia.org/wikipedia/zh/math/2/b/1/2b19a41a6ca9691cdbd5fa9f15665d5a.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Thistle}\text{Thistle}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/2/8/828c123619d3d3e078aa28bbb362c389.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{Turquoise}\text{Turquoise}" src="http://upload.wikimedia.org/wikipedia/zh/math/e/d/b/edbea9eb14e35cbadb5e2df41afae369.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{Violet}\text{Violet}" src="http://upload.wikimedia.org/wikipedia/zh/math/8/5/d/85da72dd0a892dd3364fefd94a14cf7c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{VioletRed}\text{VioletRed}" src="http://upload.wikimedia.org/wikipedia/zh/math/9/b/5/9b5d2430fd995e45f7974583ab86db0c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="background-color:black"><img alt="\pagecolor{Black}\color{White}\text{White}" src="http://upload.wikimedia.org/wikipedia/zh/math/a/e/b/aebc9cd09371478a17387abbc3b09c82.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
<tr>
<td><img alt="\color{WildStrawberry}\text{WildStrawberry}" src="http://upload.wikimedia.org/wikipedia/zh/math/0/9/6/0962e3794c0315fd26b9668555ebff1c.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td style="background-color:gray"><img alt="\pagecolor{Gray}\color{Yellow}\text{Yellow}" src="http://upload.wikimedia.org/wikipedia/zh/math/6/f/0/6f08fd94fdd641d1e7398d6762ae2545.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{YellowGreen}\text{YellowGreen}" src="http://upload.wikimedia.org/wikipedia/zh/math/7/2/a/72a3756fa95c0da850b33ccb7b3e3900.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
<td><img alt="\color{YellowOrange}\text{YellowOrange}" src="http://upload.wikimedia.org/wikipedia/zh/math/1/1/9/119eb093f2ffcbd3d77a13f55f185f52.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></td>
</tr>
</tbody>
</table></div>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<sup>＊</sup>注︰输入时第一个字母必需以大写输入，如<code>\color{OliveGreen}</code>。</p>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dt>例子</dt></dl>
<ul style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<li><code>{\color{Blue}x^2}+{\color{Brown}2x} -{\color{OliveGreen}1}</code></li></ul>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dd><img alt="\pagecolor{White} {\color{Blue}x^2}+{\color{Brown}2x} - {\color{OliveGreen}1}" src="http://upload.wikimedia.org/wikipedia/zh/math/5/9/7/5974e571c8ac33bee928deb354b8b8ae.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<br>
</p>

## **强制使用PNG**
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
假设我们现在需要一个<a target="_blank" href="http://zh.wikipedia.org/wiki/PNG" rel="nofollow" title="PNG" style="color:rgb(106,57,6); text-decoration:none">PNG</a>图的数学公式。<br>
若输入&nbsp;<code>2x=1</code>&nbsp;的话︰</p>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dd><img alt="2x=1" src="http://upload.wikimedia.org/wikipedia/zh/math/e/2/4/e24b7cbea4ac6526c7bf9687d7e61516.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
&nbsp;<wbr>　<strong>↑</strong>&nbsp;这并不是我们想要的。</p>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
若你需要强制输出一个PNG图的数学公式的话，你可于公式的最后加上<code>\,</code>（小空格，但于公式的最后是不会显示出来）。</p>
<dl style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
<dd>输入&nbsp;<code>2x=1 \,</code>的话︰</dd><dd><img alt="2x=1 \," src="http://upload.wikimedia.org/wikipedia/zh/math/2/3/7/237b4b59d46cd7db3d26d6c700550bbe.png" title="Texlive:&nbsp;<wbr>latex数学符号表(2)" style="border:none; max-width:100%"></dd></dl>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
&nbsp;<wbr>　<strong>↑</strong>&nbsp;以PNG图输出。</p>
<p style="color:rgb(54,46,43); font-family:Arial; font-size:14px; line-height:26px">
你也可以使用&nbsp;<code>\,\!</code>，这个亦能强制使用PNG图像。</p>
