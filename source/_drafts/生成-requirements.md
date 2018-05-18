---
title: 生成 requirements.txt 
tags: [Python, requirements, virtualenvs]
---
因为是项目内，首先安装虚拟环境 

Python 安装类似前端自动生成依赖到 package.json
pip 安装 package 时自动生成依赖到 requirements.txt
`pip freeze > requirements.txt`

运行后按照的packages太多了，好多并没有实际在项目中用到，改用：
`pip freeze -l > requirements.txt`