---
title: Nginx中的rewrite指令
tags:
  - nginx
categories:
  - note
abbrlink: 5179d239
date: 2021-07-04 00:00:00
---

# Nginx中的rewrite指令(break,last,redirect,permanent)

### rewite

在server块下，会优先执行rewrite部分，然后才会去匹配location块
server中的rewrite break和last没什么区别，都会去匹配location，所以没必要用last再发起新的请求，可以留空

### location中的rewirte：

不写last和break - 那么流程就是依次执行这些rewrite
\1. rewrite break - url重写后，直接使用当前资源，不再执行location里余下的语句，完成本次请求，地址栏url不变
\2. rewrite last - url重写后，马上发起一个新的请求，再次进入server块，重试location匹配，超过10次匹配不到报500错误，地址栏url不变
\3. rewrite redirect – 返回302临时重定向，地址栏显示重定向后的url，爬虫不会更新url（因为是临时）
\4. rewrite permanent – 返回301永久重定向, 地址栏显示重定向后的url，爬虫更新url

### 使用last会对server标签重新发起请求

如果location中rewrite后是对静态资源的请求，不需要再进行其他匹配，一般要使用break或不写，直接使用当前location中的数据源，完成本次请求
如果location中rewrite后，还需要进行其他处理，如动态fastcgi请求(.php,.jsp)等，要用last继续发起新的请求
(根的location使用last比较好, 因为如果有.php等fastcgi请求还要继续处理)

### 使用alias指定源：必须使用last

if语句主要用来判断一些在rewrite语句中无法直接匹配的条件,比如检测文件存在与否,http header,cookie等
