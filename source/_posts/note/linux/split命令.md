---
title: split命令
date: 2016-2-15
updated: 2016-2-16
tags:
  - split
categories:
  - note
abbrlink: aa4c47b6
---


[文件过滤分割与合并](http://man.linuxde.net/sub/%e6%96%87%e4%bb%b6%e8%bf%87%e6%bb%a4%e5%88%86%e5%89%b2%e4%b8%8e%e5%90%88%e5%b9%b6)

**split命令**可以将一个大文件分割成很多个小文件，有时需要将文件分割成更小的片段，比如为提高可读性，生成日志等。
<!--more-->

### 选项 

```
-b：值为每一输出档案的大小，单位为 byte。
-C：每一输出档中，单行的最大 byte 数。
-d：使用数字作为后缀。
-l：值为每一输出档的列数大小。
```

### 实例 

生成一个大小为100KB的测试文件：

```
1+0 records in
1+0 records out
102400 bytes (102 kB) copied, 0.00043 seconds, 238 MB/s
```


```
[root@localhost split]# ls
```

文件被分割成多个带有字母的后缀文件，如果想用数字后缀可使用-d参数，同时可以使用-a length来指定后缀的长度：

```
[root@localhost split]# ls
```

为分割后的文件指定文件名的前缀：

```
[root@localhost split]# ls
```

使用-l选项根据文件的行数来分割文件，例如把文件分割成每个包含10行的小文件：

```
```
