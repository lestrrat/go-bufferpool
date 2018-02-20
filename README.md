# go-bufferpool

Very simple bytes.Buffer pool using sync.Pool.

[![Build Status](https://travis-ci.org/lestrrat/go-bufferpool.svg?branch=master)](https://travis-ci.org/lestrrat/go-bufferpool)

[![GoDoc](https://godoc.org/github.com/lestrrat/go-bufferpool?status.svg)](https://godoc.org/github.com/lestrrat/go-bufferpool)


I got tired of writing the same sync.Pool for byte.Buffer objects.

# WARNING

This repository has been moved to [github.com/lestrrat-go/bufferpool](https://github.com/lestrrat-go/bufferpool). This repository exists so that libraries pointing to this URL will keep functioning, but this repository will NOT be updated in the future. Please use the new import path.

# SYNOPSIS


```
import "github.com/lestrrat/go-bufferpool"

var pool = bufferpool.New()

func main() {
    buf := pool.Get()
    defer pool.Release(buf)

    // ...
}
```
