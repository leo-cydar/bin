<h1 align="center">b71729/bin</h1>
<p align="center">
  <i>A set of utility interfaces for working with binary data streams.</i>
</p>

[![Go Report Card](https://goreportcard.com/badge/github.com/b71729/bin)](https://goreportcard.com/report/github.com/b71729/bin) [![Build Status](https://travis-ci.org/b71729/bin.svg?branch=master)](https://travis-ci.org/b71729/bin)

---


## Alternative packages

#### `binary`
An alternative to this package would be to use the `Read(interface{})` exposed in the `binary` package
for reading data.
Although a relatively simple interface is provided, there are some distinct advantages to using
this package over `binary.Read`:

- IDE and compile-time type checking is possible; this helps prevent bugs
- Built-in tracking of the reader's offset is provided
- A byte order can be set for subsequent calls,
    without needing to keep track of it every call
- Is ~2-3x faster in benchmarks
- Allocates no objects in the various `Read/ReadBytes/ReadXYZ` methods.
