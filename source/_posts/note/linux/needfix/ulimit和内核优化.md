---
title: ulimit和内核优化
categories:
  - needfix
date: 2021-07-04 00:00:00
---
ulimit

    vim /etc/security/limits.d/90-nproc.conf

    vim /etc/security/limits.conf


内核

    vim /etc/sysctl.conf


查看句柄及PID

    lsof -n|awk '{print $2}'|sort|uniq -c|sort -nr|more