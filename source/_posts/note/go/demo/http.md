---
title: http
tags:
  - go
categories:
  - demo
abbrlink: 97780db2
date: 2021-07-04 00:00:00
---

```golang
package main 
import "net/http"
func main() {
	http.HandleFunc("/",hello)
	http.ListenAndServe(":8080",nil)	
}
func hello(w http.ResponseWriter, r *http.Request) {
	w.Write([]byte("hello world!"))
}
```
