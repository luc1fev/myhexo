---
title: iTerm2 && oh my zsh
date: 2019-03-24 08:08:55
tags: tools
---


---

<!-- toc --> 

[出处1](https://www.jianshu.com/p/7de00c73a2bb)

## .zshrc 配置
echo export HISTSIZE=10000 >>~/.zshrc
echo setopt HIST_IGNORE_DUPS >>~/.zshrc
echo setopt AUTO_PUSHD >>~/.zshrc
## 工具插件

### install for zsh 


#### autojump 
on mac brew install autojump
vi ~/.zshrc


> remember to add your plugins into .zshrc plugins line!

### Vim 配置

> echo syntax on >> ~/.vimrc
> echo set background=dark >> ~/.vimrc
> echo set number >> ~/.vimrc


#### Vim 美化 
> git clone git://github.com/altercation/solarized.git
> mkdir -p ~/.vim/colors
> cp solarized/vim-colors-solarized/colors/solarized.vim ~/.vim/colors/


echo colorscheme solarized >> ~/.vimrc


### Lrzsz 配置

[详细](https://blog.csdn.net/sylar_d/article/details/51971585)

[zmodem github](https://github.com/mmastrac/iterm2-zmodem)

在ITerm2中对应的profile中“Advance”->"Trigger" 中填入：

在ITerm2中对应的profile中“Advance”->"Trigger" 中填入：
    
```
    Regular expression: rz waiting to receive.\*\*B0100
    Action: Run Silent Coprocess
    Parameters: /usr/local/bin/iterm2-send-zmodem.sh
    Instant: checked
```
```
    Regular expression: \*\*B00000000000000
    Action: Run Silent Coprocess
    Parameters: /usr/local/bin/iterm2-recv-zmodem.sh
    Instant: checked
```

### 安装 oh-my-zsh `zsh 主要插件`

> curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh
> or
> wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | sh

---


## 美化插件

### 用 powerline 美化  

#### 安装库



安装 pip `sudo easy_install pip`  

安装power line  `pip install powerline-status`
[github](https://github.com/powerline/powerline)


####  给iTerm2 设置 powerline字体  


#### iTerm配色

##### solarized

[solarized 方案 github](https://github.com/altercation/solarized)

用来设置 iTerm 配色

> 双击在`solarized/iterm2-colors-solarized`文件夹里的 `Solarized Dark.itermcolors` 或 `Solarized Light.itermcolors`,他会导入到 iTerm 中

> 接着在profiles 的 colors 标签右下角 color presents 选中 solarized

![color](/images/itermColor.png)


#### agnoster

这是让`oh-my-zsh`出现特殊字符的插件

[agnoster 方案 github](https://github.com/fcamblor/oh-my-zsh-agnoster-fcamblor)

> 依旧clone 文件到一个地方先

> git clone https://github.com/fcamblor/oh-my-zsh-agnoster-fcamblor.git

> cd 到包里面 `./insttall` 会安装到`~/.oh-my-zsh/themes` 中

> 接着在 zsh 的配置文件 `.zshrc` 中 把`ZSH_THEME` 后改成 agnoster 


##### 给iTerm 安装字体库  

用来让 iTerm2 显示特殊字符

> git clone https://github.com/powerline/fonts.git

> cd 到 下载的 font 里再 `./install.sh` 安装 powerline 字体库, 样式样本在 `fonts/samples/All.md` 里
> 他们会自动复制到到`/Users/superdanny/Library/Fonts`

> 这时设置iTerm2 也会有刷新.
> preferences 里点 profiles, 右边 text 里把 regular font 和 Non-Ascii font 都设置成 powerline 的字体,或者直接搜索

![截图](/images/iTemText.png)




### 高亮 highlighting 

这是在用 zsh 输入时,高亮语法的插件

> `cd ~/.oh-my-zsh`

> 到你`.oh-my-zsh/custom/plugins`包

> git clone git://github.com/zsh-users/zsh-syntax-highlighting.git`

> 编辑 `.zshrc` 

> 找到 plugins 这行后 修改为`plugins=(OtherPlugin zsh-syntax-highlingting AnotherPlugin)`

> 后面追加启动路径 `source $ZSH/custom/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh`

> 保存退出

重新开启一个对话!

---
[更多](http://macshuo.com/?p=676)




