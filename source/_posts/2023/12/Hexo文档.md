---
title: Hexo文档
date: 2023-12-05 10:39:26
categories:
- Hexo配置
tags:
- 工具使用
---

# Hexo使用文档

## 前置安装

- 安装npm：`https://nodejs.org/en/download/`
- 安装hexo：`npm install -g hexo-cli`

## 图床

### Github做图床

创建Github仓库，将图片资源推送到这个仓库。随后按照以下步骤生成图片的外链：

- 进入Github仓库，查看图片资源，从而获得图片访问地址，形如：`https://github.com/yqw-nku/yqw-nku.github.io/blob/blog_source/images/common/yqw.jpg`
- 修改链接里的blob为raw，得到`https://github.com/yqw-nku/yqw-nku.github.io/raw/blog_source/images/common/yqw.jpg`，这就是最终的图片外链地址

## Hexo-Git仓库使用

目前已推送blog_source分支存储Hexo搭建时的源码，但是node_modules目录没有上传（放到是主题信息，.gitignore里忽略了），所以当一台新设备拉取仓库后，需要先执行`npm install --save hexo-theme-fluid`安装主题才可以继续使用。
