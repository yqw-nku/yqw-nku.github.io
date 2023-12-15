---
title: Goland使用
date: 2023-12-10 12:05:09
categories:
- 工具使用
tags:
- GOLANG
---

### Goproxy设置

- 推荐两个代理地址：
  - 阿里云 `https://mirrors.aliyun.com/goproxy/`
  - goproxy.io的 `https://goproxy.io/` 
- 在Goland里打开"settings-Go-Go Modules"，在Environment设置GOPROXY，例如：`GOPROXY=https://mirrors.aliyun.com/goproxy/`

- 在Goland里新打开一个termnial，`go env`，GOPROXY已经被修改。



