# HexoBlog

## 分支说明

Hexo+GitHub搭建博客步骤其实就是：

- 先拉取一个已存在的hexo模板git仓库
- 在仓库里写入自己的MarkDown笔记
- 依赖Hexo+Npm工具将笔记生成Hexo博客需要的源文件
- 将生成的源文件推送到指定的远端仓库指定分支

基于此，为了方便管理，只创建一个Git仓库，用不同分支存储不同数据：

- `blog_source`分支：存储搭建博客的源文件（包括Markdown笔记）
- `master`分支：存储Hexo生成的博客文件（由于github page只能识别`master`分支，所以博客文件一定要在`master`分支）

因此，一般只要操作`blog_source`分支代码和文件，`master`分支由Hexo工具生成和推送。