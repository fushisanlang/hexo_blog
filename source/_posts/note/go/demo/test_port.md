---
title: test_port
tags :
 - go
categories:
 - demo
---

```golang
package main

import (
	"fmt"
	"net"
)

var address_str string

func main() {
	fmt.Scanln(&address_str)
	_, err := net.Dial("tcp", address_str)
	if err != nil {
		fmt.Println(address_str + " is error,check it!!!")
	}
}

```
