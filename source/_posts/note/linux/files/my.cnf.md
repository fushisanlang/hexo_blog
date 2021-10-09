---
title: my.cnf
tags:
  - mysql
categories:
  - file
abbrlink: a4b910a9
date: 2021-07-04 00:00:00
---
```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
# Disabling symbolic-links is recommended to prevent assorted security risks
symbolic-links=0
[mysqld_safe]
log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid
```
