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

   ![Alt](https://github.com/yqw-nku/yqw-nku.github.io/raw/blog_source/images/2023-12/1.png)

2. 进入main.go所在目录，执行：`dlv debug`

### **调试指令-断点管理**

| 指令        | 缩写 | 用法             | 案例  |
| ----------- | ---- | ---------------- | ----- |
| break       | b    | 设置断点         | case1 |
| breakpoints | bp   | 查看当前所有断点 | -     |
| clear       | /    | 删除断点         | -     |
| clearall    | /    | 删除多个断点     | -     |
| toggle      | /    | 启用或关闭断点   | -     |

### **调试指令-程序执行**

| 指令     | 缩写 | 用法                             | 案例 |
| -------- | ---- | -------------------------------- | ---- |
| continue | c    | 继续执行到一个断点或者程序结束码 |      |
| next     | n    | 执行下一行代码                   |      |
| restart  | r    | 重新执行程序                     |      |
| step     | s    | 执行代码的下一步                 |      |
| stepout  | so   | 跳出当前执行函数                 |      |

### **调试指令-参数管理**

| 指令    | 缩写 | 用法                                                         | 案例   |
| ------- | ---- | ------------------------------------------------------------ | ------ |
| args    | /    | 打印函数input                                                | case18 |
| display | /    | 打印加入到display的变量的值，每次执行下一行代码或下一个断点时 | case19 |
| locals  | /    | 打印局部变量                                                 | case20 |
| print   | p    | 打印表达式的结果                                             | case21 |
| set     | /    | 设置某个变量的值                                             | case22 |
| vars    | /    | 查看全局变量                                                 | case23 |
| whatis  | /    | 查看变量类型                                                 | case24 |

### **调试指令-其他**

| 指令  | 缩写     | 用法                   | 案例   |
| ----- | -------- | ---------------------- | ------ |
| exit  | quit / q | 退出                   | case26 |
| funcs | /        | 打印程序用到的所有函数 | case27 |
| help  | h        | 帮助信息               | case28 |
| list  | ls / l   | 打印代码               | case29 |



