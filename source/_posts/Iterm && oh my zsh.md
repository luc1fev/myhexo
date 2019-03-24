---
title: iTerm2 && oh my zsh
date: 2019-03-24 08:08:55
tags: 工具使用
---





---

[TOC]

<!-- toc-->

[出处1](https://www.jianshu.com/p/7de00c73a2bb)

# iTerm 2 相关

## 主题/色彩/字符



## 插件配置

### Lrzsz 配置

[详细](https://blog.csdn.net/sylar_d/article/details/51971585)

[zmodem github](https://github.com/mmastrac/iterm2-zmodem)

在ITerm2中对应的profile中“Advance”->"Trigger" 中填入：

```
    在ITerm2中对应的profile中“Advance”->"Trigger" 中填入：
    Regular expression: rz waiting to receive.\*\*B0100
    Action: Run Silent Coprocess
    Parameters: /usr/local/bin/iterm2-send-zmodem.sh
    Instant: checked

    Regular expression: \*\*B00000000000000
    Action: Run Silent Coprocess
    Parameters: /usr/local/bin/iterm2-recv-zmodem.sh
    Instant: checked
```

### 安装 oh-my-zsh `zsh 主要插件`

`curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh`

or

`wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | sh`

### 安装 power line `样式`

[github](https://github.com/powerline/powerline)

查看 power line 状态 `pip install powerline-status`

安装 power line `sudo easy_install pip`

### 安装字体库

cd 到 install.sh 再 ./install.sh 安装 powerline 字体库

会自动到`/Users/superdanny/Library/Fonts`

### 设置 iTerm2 字体

preferences 里点 profiles, 右边 text 里把 regular font 和 Non-Ascii font 都设置成 powerline 的字体

### 配色

#### solarized

[solarized 方案 github](https://github.com/altercation/solarized)

用来设置 iTerm 配色

在方案里 `solarized/iterm2-colors-solarized`  双击 `Solarized Dark.itermcolors` 和 `Solarized Light.itermcolors` 导入到 iTerm 中

接着在profiles 的 color 中 load presents 选中 solarized 

#### agnoster

[agnoster 方案 github](https://github.com/fcamblor/oh-my-zsh-agnoster-fcamblor)

用来设置`oh-my-zsh`命令行特殊字符

在包里面 `./insttall.sh` 会安装到`~/.oh-my-zsh/themes` 中

再在 zsh 的配置文件 `.zshrc` 中 把`ZSH_THEME` 后改成 agnoster 

#### 高亮 highlighting (感觉有问题)

`git clone git://github.com/zsh-users/zsh-syntax-highlighting.git`

接着在 `.zshrc` 中添加 `source XXX/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh`

同时 到`~/.oh-my-zsh/custom/plugins` 中打开 `.zshrc` 添加`plugins=(zsh-syntax-highlingting)`