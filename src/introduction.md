# Introduction

Groan Selection Language (GSL) is a query language for selecting atoms in the [`groan_rs`](https://github.com/Ladme/groan_rs) crate and in programs built on top of it, such as [`gorder`](https://github.com/Ladme/gorder) or [`gcenter`](https://github.com/Ladme/gcenter).

The selection language is quite similar to the languages used by [VMD](https://www.ks.uiuc.edu/Research/vmd/) and [MDAnalysis](https://www.mdanalysis.org/), so if you are familiar with them, GSL should feel quite intuitive. This guide should help you understand and efficiently use GSL both when working directly with the `groan_rs` library and when using applications built on top of it.

***

*This document describes the syntax of GSL v0.9 (corresponding to `groan_rs` v0.9 and v0.10).*