---
title: "GoDoc in Local"
date: 2021-11-05T10:05:11+08:00
tags: [golang, godoc]
draft: false
---

In your preferred directory, initialize GOPATH using the short script in [Suggested GoLang Init Script](https://ismael.casimpan.com/quicktasks-golang/suggested-init-script-before-coding-in-golang/).

Then, do the following steps:

1. Install godoc

```
~$ go install golang.org/x/tools/cmd/godoc@latest
go: downloading golang.org/x/tools v0.1.7
go: downloading golang.org/x/sys v0.0.0-20210809222454-d867a43fc93e
go: downloading golang.org/x/xerrors v0.0.0-20200804184101-5ec99f83aff1
go: downloading golang.org/x/net v0.0.0-20210805182204-aaa1db679c0d
go: downloading github.com/yuin/goldmark v1.4.0
go: downloading golang.org/x/mod v0.4.2
```

2. Run godoc
```
~$ godoc
using module mode; GOMOD=/dev/null
```

It defaults to using port 6060.

If default port has a conflict, replace it by using parameter `-http=:NNNN` where NNNN is your port number.

Example, if port `9999` is available, you can run godoc as follows:
```
~$ godoc -http=:9999
using module mode; GOMOD=/dev/null
```

3. In your browser, you can now go to http://localhost:6060/pkg/ or whatever custom port you used. 
