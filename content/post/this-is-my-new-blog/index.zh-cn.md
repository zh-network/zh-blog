---
title: 这是涵的新博客！
description: 以后就在这里投稿一些高质量的生活点滴和技术点滴，学习和实验记录等等，大家多多关照w～
date: 2022-11-17
slug: this-is-my-new-blog
image: zh-20221002-middle0finger.jpg
categories:
    - ZH
    - 涵
    - 生活
    - 技术
---

## 引言

涵是用Hugo主题stack搭建的新博客，不知道为什么总是嫌弃原来使用的 Wordpress 各种奇妙的问题，不过真正的原因还是我太菜了w；所以本文介绍一下该Hugo大概是如何搭建出来的w  

## QuickStart（涵用的是 MacOS 所以以下过程由Mac举例）

```
# 安装 Hugo: 
brew install hugo

# 本地创建一个Hugo网站
hugo new site zh-blog && cd zh-blog

# 下载stack主题
git init
git clone https://github.com/CaiJimmy/hugo-theme-stack/ themes/hugo-theme-stack

# 将实主题模板移动到博客根目录下
cp -r themes/hugo-theme-stack/exampleSite/* ./

# 删除config.toml以防冲突，之后配置文件使用config.yaml
rm config.toml
remove config.toml? y

# 构建静态网站文件，并启动本地http调试服务
hugo server
```

然后在本地服务器打开浏览器，输入 [http://localhost:1313](http://localhost:1313) 即可预览示例网站

# 文件架构
```
.
├── archetypes                  
│   └── default.md
├── config.yaml                 # 网站配置文件
├── content                     # 站点内的内容都在这里
│   ├── categories              # “分类”页面的首页
│   │   └── Test                # “分类”页面下的一个分类页面
│   ├── page                    # 显示在网站主页左侧边栏菜单的选项
│   │   ├── about               # 左侧边栏菜单中的“关于”页面
│   │   ├── archives            # 左侧边栏菜单中的“归档”页面
│   │   ├── links               # 左侧边栏菜单中的“链接”页面
│   │   └── search              # 左侧边栏菜单中的“搜索”页面
│   └── post                    # 用户写的帖子都放在这里，每个子文件夹对应一个帖子
│       ├── chinese-test
│       ├── emoji-support
│       ├── markdown-syntax
│       ├── math-typesetting
│       ├── placeholder-text
│       └── rich-content
├── data
├── layouts
├── LICENSE
├── README.md
├── resources
│   └── _gen
│       ├── assets
│       └── images
├── static                     # 放用户自定义字体、用户头像、网站小图标等
└── themes                     # 放各种主题
    └── hugo-theme-stack       # stack主题
        ├── archetypes
        ├── assets
        ├── config.yaml
        ├── data
        ├── debug.sh
        ├── exampleSite
        ├── go.mod
        ├── i18n
        ├── images
        ├── layouts
        ├── LICENSE
        ├── netlify.toml
        ├── README.md
        └── theme.toml

```
只要按照自己的需求去修改就好啦！默认的测试页文件给你安排的明明白白的～换头像只需要换掉 ``` themes/hugo-theme-stack/assets/img/avatar.png ``` 文件就好啦！