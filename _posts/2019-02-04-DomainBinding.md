---
layout: post
title: 为Github Pages绑定域名
class: Technology
categories: ["Personal Blog"]
keywords: Github Pages, Domain, 域名, Godaddy, DNSPOD
---

为Github Pages绑定域名需要**购买域名**，**DNS解析**，**Github注册域名**三个步骤。

## **购买域名**
有很多提供商可以选择，国内的域名注册商有万网，阿里云，腾讯云等。国外的域名注册商有Godaddy等。价格基本大同小异，.cn后缀的域名较.com要便宜一些，但是需要在国内注册备案，个人网站这种没什么敏感信息的站点就怎么方便怎么来了。我最终选择了Godaddy，隐隐觉得在国内域名商买的域名未来总会受到监管XD

好名字要么太贵要么都被注册了，我最后为本站注册了<www.minghao23.com>这个域名，一年￥58，Godaddy支持支付宝支付。

## **DNS解析**
Godaddy自己是有域名解析服务的，但是很多人说有被墙的风险，且解析速度在国内较慢，为了保险我还是选择了腾讯云下的DNSPOD提供解析服务， 当然你也可以选择阿里云等其他服务商。所以第一步是将Godaddy中你的域名的解析服务委托到DNSPOD。

先注册DNSPOD的账号，然后在域名解析中添加注册好的域名，打开记录管理，会有两个默认的NS记录，如下图。

![](/images/blog/WX20190204-142959@2x.png)

在Godaddy中选择自己的域名，在Nameservers中将默认的服务商改为上图的两个地址并保存。

![](/images/blog/WX20190204-143147@2x.png)

回到DNSPOD，添加如下两个CNAME记录。这个地方网上好多教程，甚至Github的官方文档都是要先添加指向Github IP地址的A记录，但是设置完了都没有成功，原github.io地址和自己注册的地址都访问不了。**其实根本不用设置A记录，只添加两个CNAME即可**，目的是解析以www开头或省略www的域名。主机记录选择@和www，记录类型选择CNAME，记录值填写个人网站提供商的给的原网址，例如我的是<minghao23.github.io>，TTL默认为600。服务商分配DNS需要花费10分钟或更长的时间，耐心等待即可。

![](/images/blog/WX20190204-143243@2x.png)

## **Github注册域名**
最后还需要在Github Pages项目的Setting中绑定你注册的域名，实现双向认证。如下图，在Custom Domain里填写你的域名即可。项目会自动在根目录下生成CNAME文件，内容就是你的域名，直接更改CNAME文件效果相同。

![](/images/blog/WX20190204-145006@2x.png)

登录你的域名试试看吧。
