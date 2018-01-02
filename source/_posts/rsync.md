---
title: rsync同步
tags:
  - rsync
  - 权限
date: 2018-01-02 15:49:05
---

- -v 显示rsync运行的日志
- --rsync-path 指定远程机器上要运行的程序以启动远程rsync进程
    - 所以把nginx配置挪到aa服务器的rsync命令是：
    ```
    rsync -v --rsync-path="sudo rsync" file.conf aa:/etc/nginx/sites-available/
    ```