---
title: HTTP request failed  与 curl (35) SSL connect error 异常
categories:
  - needfix
abbrlink: 770b0c4
date: 2021-07-04 00:00:00
---
## HTTP request failed  与 curl: (35) SSL connect error 异常


#### 现象：
```shell
git clone https://github.com/*
fatal: HTTP request failed  

curl 'https://github.com/*'
curl: (35) SSL connect error
```

#### 解决办法：
```shell
yum -y update nss
```

