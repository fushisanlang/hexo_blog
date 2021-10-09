---
title: tomcat使用软连接
categories:
  - needfix
date: 2021-07-04 00:00:00
---
  在context.xml文件中的
<Context>中 
加入
  <Resources allowLinking="true" />
并重启tomcat