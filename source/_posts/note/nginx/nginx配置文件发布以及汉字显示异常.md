---
date: 2021-07-04
title: nginx配置文件发布以及汉字显示异常
tags :
 - nginx
categories:
 - note 
---

### nginx配置文件发布以及汉字显示异常



* nginx配置文件发布

```
    autoindex_exact_size off;
    autoindex_localtime on;
    autoindex on;

```

* nginx配置文件发布汉字显示异常

```
    default_type 'text/html';
    charset utf-8;
```



