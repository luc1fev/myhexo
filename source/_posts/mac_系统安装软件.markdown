Title: Mac 系统安装软件
Notebook: 日常运维
Tags: evnd

[TOC]
#2017
## 9/25 中下午
通过 brew 在 mac 上安装了 mysql

>这是最后的信息

>We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

>MySQL is configured to only allow connections from localhost by default

>To connect run:
    mysql -uroot

>To have launchd start mysql now and restart at login:
  brew services start mysql
>Or, if you don't want/need a background service you can just run:
  mysql.server start

### 9/25 之前一直不能关机是因为 mysql 和系统的问题
一直感觉是 mysql 后来通过https://www.zhihu.com/question/50940249 安装了新mysql 解决了问题

## 9/25 下午
安装了 iterm2 代替 Terminal

## 9/26 下午
安装 EVND `evernote down` 在 atom 上

>关联了 `/Users/Cd_mbp/Documents/notesToEvernotes` 到 `~/.atom/evnd`
>把`/Users/Cd_mbp/Documents/notesToEvernotes` git 初始化了
>通过 `apm install` 在 `iterm2` 上安装了 `ever-notedown`
>>修改 `atom` 上 `grammars spell-check` 的
>> `ource.asciidoc, source.gfm, text.git-commit, text.plain, text.plain.null-grammar`
>>为
`[source.asciidoc, source.gfm, text.git-commit,`

>>`text.plain, text.plain.null-grammar, source.litcoffee,`

>>`text.markdown.evnd.mathjax.source.litcoffee.inline.html,`

>>`text.markdown.evnd.mathjax.source.gfm.inline.html,`
>>`text.markdown.evnd.source.gfm.inline.html]`

## 9/27 中午
在 atom 上 安装了`git-plus`

## 10/5 3am
使用keygen 的时候 安装了 xcode 的 command line tools

破解了 alfred, 在里面放入了一个创建Omni active的 workflow 
