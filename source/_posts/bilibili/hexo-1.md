---
title: hexo-1
tags :
 - hexo
categories:
 - bilibili
---

## 下载git bash
https://git-scm.com/downloads

## 下载node.js
http://nodejs.cn/download/

## 安装hexo

```
npm install cnpm --registry=https://registry.npm.taobao.org
cnpm install hexo
hexo init myblog
```

## 配置hexo
```
deploy:
  type: git
  repo: git@github.com:fushisanlang-13/fushisanlang-13.github.io.git
  branch: master #main
```
这里要注意缩进，每行有两个空格的缩进

## 配置ssh
```
ssh-keygen -t rsa -C 'email'  #注意替换邮箱地址
```

## 部署hexo
```
cnpm install hexo-deployer-git  --save

#这两句视频里没有，是我剪视频时候忘了加字幕了，也需要输入进去
git config user.name '用户名' #注意替换用户名
git config user.email '邮箱' #注意替换邮箱

hexo g
hexo d
```