---
layout: wiki
title: Git
categories: Git
description: Git 常用操作记录。
keywords: Git, 版本控制
---

## 常用命令

| 功能                      | 命令                                  |
|:--------------------------|:--------------------------------------|
| 添加文件/更改到暂存区     | git add filename                      |
| 添加所有文件/更改到暂存区 | git add .                             |
| 提交                      | git commit -m msg                     |
| 从远程仓库拉取最新代码    | git pull origin master                |
| 推送到远程仓库            | git push origin master                |
| 查看配置信息              | git config --list                     |
| 查看文件列表              | git ls-files                          |
| 比较工作区和暂存区        | git diff                              |
| 比较暂存区和版本库        | git diff --cached                     |
| 比较工作区和版本库        | git diff HEAD                         |
| 从暂存区移除文件          | git reset HEAD filename               |
| 查看本地远程仓库配置      | git remote -v                         |
| 回滚                      | git reset --hard 提交SHA              |
| 强制推送到远程仓库        | git push -f origin master             |
| 修改上次 commit           | git commit --amend                    |
| 推送 tags 到远程仓库      | git push --tags                       |
| 推送单个 tag 到远程仓库   | git push origin [tagname]             |
| 删除远程分支              | git push origin --delete [branchName] |
| 远程空分支（等同于删除）  | git push origin :[branchName]         |
| 查看所有分支历史          | gitk --all                            |
| 按日期排序显示历史        | gitk --date-order                     |

## Q&A

### gitignore忽略文件并删除仓库索引
有时候再创建或修改.gitignore之前，文件已经push到仓库里了，这时过滤规则对原先仓库中的文件是不起作用的，需要手动删除仓库索引。

```sh
git rm -r --cached 文件名
```

`-r`表示递归删除文件夹，`--cached`表示删除仓库索引，保留本地，文件名可以为目录。

### Git pull/push 特别慢的解决方案

用自己的 Mac 在家 git pull 的时候速度一直是2kb/s，每次都导致超时，需要修改hostname加速。

1.获取Github相关网站的ip

访问 <https://www.ipaddress.com> ，找到页面中下方的IP Address Tools - Quick Links，分别输入github.global.ssl.fastly.net和github.com，查询ip地址。

2.修改本地host文件

Mac为例，命令行下输入：`sudo vi /etc/host`，然后输入电脑的密码，打开host文件。

Window为例 `C:\Windows\System32\drivers\etc`

3.增加host映射

参考如下，增加github.global.ssl.fastly.net和github.com的映射。

```sh
151.101.185.194 github.global.ssl.fastly.net
192.30.253.112 github.com
```
4.重启终端

最后速度变成了几十kb/s吧，总之是不会超时了