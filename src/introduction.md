# Introduction

Groan Selection Language (GSL) is a query language for selecting atoms in the [`groan_rs`](https://github.com/Ladme/groan_rs) crate and in programs built on top of it, such as [`gorder`](https://github.com/Ladme/gorder) or [`gcenter`](https://github.com/Ladme/gcenter).

The selection language is quite similar to the languages used by [VMD](https://www.ks.uiuc.edu/Research/vmd/) and [MDAnalysis](https://www.mdanalysis.org/), so if you are familiar with them, GSL should feel quite intuitive. This guide should help you understand and efficiently use GSL both when working directly with the `groan_rs` library and when using applications built on top of it.

> [Click here](raw.html) for an LLM-friendly version of the entire guide. You can then copy it to your LLM of choice and ask questions about the language.

***

*This document describes the syntax of GSL v0.11 (corresponding to `groan_rs` v0.11).*