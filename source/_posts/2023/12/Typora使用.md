---
title: Typora使用
date: 2023-12-10 11:54:57
categories:
- 工具使用
---

- Typora下载地址：`https://www.123pan.com/s/HQeA-UX1Sh`
- 主题下载地址：`https://theme.typoraio.cn/theme/Ladder/`
- 自定义快捷键：

  - 进入"文件-偏好设置-通用"，点击"高级设置-打开高级设置"

  - 打开`conf.user.json`文件，在`keyBinding`的value里加上键值对。key就是在Typora里你看到的功能名字，val就是你要的快捷键组合方式（组合符号是+）。

    ```json
    "keyBinding": {
    	"代码": "Ctrl+Shift+C",
      }
    ```

  - 修改后，重启Typora生效
