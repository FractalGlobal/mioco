
<p align="center">
  <a href="https://travis-ci.org/dpc/mioco">
      <img src="https://img.shields.io/travis/dpc/mioco/master.svg?style=flat-square" alt="Travis CI Build Status">
  </a>
  <a href="https://ci.appveyor.com/project/dpc/mioco/branch/master">
      <img src="https://ci.appveyor.com/api/projects/status/p5rjfbqw2a3pxc4o/branch/master?svg=true" alt="App Veyor Build Status">
  </a>
  <a href="https://crates.io/crates/mioco">
      <img src="http://meritbadge.herokuapp.com/mioco?style=flat-square" alt="crates.io">
  </a>
  <a href="https://gitter.im/dpc/mioco">
      <img src="https://img.shields.io/badge/GITTER-join%20chat-green.svg?style=flat-square" alt="Gitter Chat">
  </a>
  <br>
  <strong><a href="//dpc.github.io/mioco/">Documentation</a></strong>
</p>

# mioco

Mioco provides green-threads (aka fibers) like eg. Goroutines in Go, for Rust.

## Status

This repo is a complete re-implementation of mioco. The code of previous
versions was moved to [mioco.pre-0.9][mioco-pre-0.9].

[mioco-pre-0.9]: https://github.com/dpc/mioco.pre-0.9

The goals of new implementation:

* [x] switch to latest `mio` version
* [x] copy all the applicable good ideas from `tokio` reactor code
* [x] simplify the approach
  * [x] remove the exposed scheduler
* [x] model the API to be more like `std` library, less like `mio`
* [ ] focus on synchronization primitives first
* [ ] support async file IO (via worker threads)
* [ ] port all the existing mioco features, tests, examples etc.
