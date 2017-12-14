---
title: vue-build-when-file-didnot-update-to-git-server
date: 2017-12-14 14:33:45
tags: [vue, build, vscode, rsync]
---
遇到一个奇怪的问题
为了方便开发
我在本地开发vue时，用rsync一类的vscode插件同步代码到服务器了
再在服务上直接npm run build
不知道为啥，执行的时候，rsync同步过来的文件都没有被成功打包
