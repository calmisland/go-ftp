# goftp #

[![Build Status](https://travis-ci.org/jlaffaye/ftp.svg?branch=master)](https://travis-ci.org/jlaffaye/ftp)
[![Coverage Status](https://coveralls.io/repos/jlaffaye/ftp/badge.svg?branch=master&service=github)](https://coveralls.io/github/jlaffaye/ftp?branch=master)
[![Go ReportCard](http://goreportcard.com/badge/jlaffaye/ftp)](http://goreportcard.com/report/jlaffaye/ftp)
[![godoc.org](https://godoc.org/github.com/calmisland/go-ftp?status.svg)](http://godoc.org/github.com/calmisland/go-ftp)

A FTP client package for Go

## Install ##

```
go get -u github.com/calmisland/go-ftp
```

## Example ##

```go
c, err := ftp.Dial("ftp.example.org:21", ftp.DialWithTimeout(5*time.Second))
if err != nil {
    log.Fatal(err)
}

err = c.Login("anonymous", "anonymous")
if err != nil {
    log.Fatal(err)
}

// Do something with the FTP conn

if err := c.Quit(); err != nil {
    log.Fatal(err)
}
```
