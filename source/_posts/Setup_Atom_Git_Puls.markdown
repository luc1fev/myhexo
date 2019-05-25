## 关于github 的 ssh 连接

[TOC]


想用 atom 去推送 一些文件到自己的 github 作为保存
于是下载了 `git- plus` 插件
>并且无意中得知 atom 是基于 web 的 app

>很多东西都可以用 css 重新编辑 并且还有音乐播放功能,但缺点就是太慢

>并且目前版本 `1.20.1` 并不能支持markdown 的 flow

鉴于之前一直都没有使用 github 的 ssh 版 所以得重新弄.

## 首先是设置 ssh key

[参考](http://www.jianshu.com/p/b81eeb5d7858)

>鉴于一直使用桌面版的 github,并且账户里`SSH & GPG keys `似乎已经有了一个 ssh key,

>所以没有按里面说的删除 ssh key,重新新建一个

>而是删除`SSH & GPG keys` 该设备的 key , 接着重新复制 /.ssh/xx_rsa.pub 的内容
    ,新建了一个 SSH key.

结果说跟之前一样.  &nbsp; &nbsp;  :(

接着一切顺利的连接到了 Github,没有遇到 文中遇到的问题.

创建了新的 repository 之后就准备上传了.


## remote: error: GH007: Your push would publish a private email address.
> 中间跳过了很多 git 初始化,commit之类的设置

[参考](http://blog.csdn.net/neuldp/article/details/76737010)

因为我使用了不公开显示我的 email 所以在上传文件的时候遇到了这个问题.

我使用了他第一个方法解决了问题

大致描述如下
>重新用`你的公开 email `设置为全球变


>重新用`你的公开 email `设置为该项目的 用户邮箱

>撤回并重新设置最后一次的 commit

>push

## 多次需要输入用户名和密码的问题
应该是在我 push 的时候遇到的,具体我也忘记了

这个是由于错误的拿了 `HTTPS` 地址作为 `SSH` 地址作为 push 地址
>把地址从`https://`改成`git@` 就好


    在 ssh 上面成功 push 了一遍,再用 'git-plus' 推一遍

## 提交的时候经常显示成功 但并没有显示在 github 上

> 重新走了一遍流程就可以了,我也不知道为什么

    好了.就这样结束了. 对于普通的push 和 pull`新初始化的经常需要先 pull 才能提交` 都可以操作了

    剩下会涉及到 删除某些 commit 或者其他操作,具体用到的时候再继续 
