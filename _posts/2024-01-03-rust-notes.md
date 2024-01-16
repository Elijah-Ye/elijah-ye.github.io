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

`Trait:` a collection of methods in Rust.  i.e. In OOD (Object Oriented Design) there are abstract classes and interfaces. In Functional Language, there are type classes.

`try.into()` returns `Result` which canbe success or fail. If fail, it will terminate the current program. 

Due to the nature of floating point numbers, **avoid using floating point equality**.

### Rational, Complex and different number types
**Static method** is a function that's available for a type, but it's not an instance of that type. **Instance method** operates on the instance of the type. **Static method** associated with the type, but you can call it without having an existing instance of the type, like `new()`.

Use `new()` if you can. It involves less clutter. 

### Flow Control
```rust
for item in container {
  // some code
}
```

<br>

There are some **pitfalls** in Rust's flow control:
  
  - Once `container` is accessed, it becomes invalid.
  - Reuse requires `&container`.
  - Modify the item in the requires `&mut container`.

<br>

**Range-based for loop**
```rust
for _ in 0..10 {
  //some code
  // 0..10 is excluding 10
  // 0..=10 is including 10
}
```
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/for_loop.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

<br>

**while & loop**
```rust
loop {
  // some code
  // this is mainly used for servers
}
```

<br>

**Break out a nested loop via labels**
```rust
'outer: for x in 0.. {
  for y in 0.. {
    for z in 0.. {
      if x + y + z > 1000 {
        break 'outer;
      }
 
      // ...
    }
  }
}
```
<br>

**Rust has no `goto`**

<br>

**Conditional Statements**
```rust
if (){
  // in rust there is no "truthy" or "falsey" statements
  // unlike C/C++, where 0 means false and 1 means true
  // in rust, there is only true or false
}
else if (){

}
else {

}
```
<br>

`match` is like `switch` in C/C++. However, `match` needs all possible options to be handled. 
```rust
fn main() {
  let needle = 42;
  let haystack = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
 
  for item in &haystack {
    let result = match item {
      42 | 132 => "hit!",
      _ => "miss", // _ means all other cases 
    };
 
    if result == "hit!" {
      println!("{}: {}", item, result);
    }
  }
}
```

<br>

### Defining Functions
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/function.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<br>

### Using References
`reference` is a value that stands in place for another value.

`&` and `*` are used for reference and dereference. These operators act as unary operators, meaning that these only take one operand. 





