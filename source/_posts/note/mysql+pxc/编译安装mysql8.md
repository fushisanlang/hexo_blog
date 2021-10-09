---
title: 编译安装mysql8
tags:
  - mysql8
categories:
  - note
abbrlink: b98497bd
date: 2021-07-04 00:00:00
---

### 编译安装mysql8



```shell
cmake -DCMAKE_INSTALL_PREFIX=/data/mysql8 -DDEFAULT_CHARSET=utf8 -DDEFAULT_COLLATION=utf8_general_ci -DWITH_EXTRA_CHARSETS=all -DSYSCONFDIR=/etc -DDOWNLOAD_BOOST=1 -DWITH_BOOST=. && make && make install

bin/mysqld --defaults-file=/etc/my8.cnf --initialize --user=mysql

./bin/mysqld_safe --defaults-file=/etc/my8.cnf --user=mysql 

create user  'root'@'%' IDENTIFIED BY '11'

 GRANT ALL PRIVILEGES ON *.* TO 'root'@'%'   WITH GRANT OPTION;

```

