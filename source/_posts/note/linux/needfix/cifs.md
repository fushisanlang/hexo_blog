---
title: cifs
categories:
  - needfix
abbrlink: b57a9bf9
date: 2021-07-04 00:00:00
---
* cifs


    yum install samba-client
    smbclient -L //ip
    smbclient //ip/sharename
    #或
    mount //ip/sharename /mountpoint -o username=guest
    vim /etc/fstab
    //ip/sharename /mountpoint cifs	defaults,username=guest 0 0
    mount -a
