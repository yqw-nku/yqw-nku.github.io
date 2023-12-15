---
title: Golang配置
date: 2023-12-15 10:08:22
categories:
- GOLANG之旅
tags:
- GOLANG
---

# Golang调试工具-Delve

## 安装

在已经安装了Golang的前提下，按以下步骤安装调试工具delve：

1. 使用`go env`命令查看`GOPATH`取值，一般是`/root/go`
2. 配置环境变量：`export GOPATH=/root/go`
3. 进入根目录，安装delve：`go install github.com/go-delve/delve/cmd/dlv@latest`
4. 配置链接：`ln -s ${GOPATH}/bin/dlv /usr/local/bin/dlv`

## 使用

### 启动调试

进入调试模式，有两种模式，推荐第一种：

1. 先编译，得到二进制，然后采用`dlv exec {bin_path}`
2. 直接接入：`dlv main.go`
