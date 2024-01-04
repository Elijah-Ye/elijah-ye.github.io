---
layout: post
title: a collection of notes on Rust language
date: 2024-01-03 15:30:00-0400
description: my personal notes from the book Rust in Action
tags: notes
categories: personal posts
giscus_comments: false
related_posts: false
toc:
  sidebar: left
---
This post shows how to add a table of contents in the beginning of the post.

## Chapter 1 Introducing Rust

### hello world for Rust

```rust
fn main() {
  println!("Hello,world!");
}
```
That's what Rust's hello world looks like.

Rust `cargo` tools -> download and compile dependencies

`.rs` is Rust

In Ruby, `!` is used to signal a destructive operation, meaning alter the original contents.

In Rust, `!` is used to signal the use of a "macro" (like functions).

Rust is an `expression-based language`

```rust
let varName: type = ...;
```

In Rust, `let` allows Rust to infer the type of elements, like `auto` in c/c++.

`if let` conditionally processing data.

### Initial introduction to Cargo

`cargo` is a front=end for rustc -> rust compiler

`$ cargo new` creates a new directory

`$ cargo init` create within the directory

`$ cargo build` downloads dependencies and compiles the code

`$ cargo run` runs `cargo build` then runs the executable files

`$ cargo run --release` skips conditional compile

`$ cargo run -q --release`: `-q` stands for quiet, it will further reduce the output code.

`$ cargo doc` builds a html documentation for the project

### Summarize intro to Rust

Rust is high control + high safety.

&nbsp; Python -> high safety + low control

&nbsp; C/C++ -> high control + low safety

Rust is labelled as a `system programming language`

`()` is pronounced unit -> when no other meaningful return value, expression return `()` -> unit.

Rust uses arrays to hold data by default, so it is "cache friendly".

**Downside of Rust:**
- Cyclic data structure. i.e. doubly linked-list
- Compile time is longer for Rust

**Where Rust used the most ?**
- Commandline Untilitize
- Data processing -> fastest Regular Expression Engine

**3 Main commandline tools for Rust**
1. cargo
2. rustup (rust install)
3. rustc



## Chapter 2 Language Fundations

1. Using `rustc` to compile
2. `cargo` > `rustc`, since `cargo` helps you to figure out dependencies as well

Code blocks also known as lexical scopes.

Variable bindings: bind variable name and its value together

Variables are immutable by default, but you can use `mut` keyword to change that.

```rust
let varName: type = ...;
```

```rust
fn add(...) -> i32 {} //i32 is the return type in this context
```

Rust also has `Operator Overload` like C/C++

Numbers have methods. Rust uses `24.5_f32.round()` rather than `round(24.5_f32)`

`_` means nothing in numbers. It is good for enhancing readability.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/rust_number_types.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

### Compare between types
```rust
fn main() {
  let a: i32 = 10;
  let b: u16 = 100;
  
  if a < b.into() {
    println!("Ten is less than one hundred.");
  }
}
```
