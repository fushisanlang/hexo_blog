---
title: jdk openssl证书
categories:
  - needfix
date: 2021-07-04 00:00:00
---
```
cd /usr/java/jdk1.6.0_45/jre/lib/security
keytool -list -keystore cacerts -storepass changeit | grep digicertglobalrootca
keytool -list -keystore cacerts -storepass changeit | grep baltimorecybertrustca
```