# Rust

## Cargo

- Cargo is Rust's package manager

- `cargo new` starts a new cargo project
- `cargo build` builds a project
- `cargo run` builds and runs a project in one step
- `cargo check` checks for errors without generating a binary
- `cargo build --release` compiles the code with optimizations

## Basics

- `use std::io;` brings the input/output (io) standard library into scope

- `let mut apples = 5;` In Rust, variables are immutable by default. mut creates a mutable variable

- `String::new()` returns a new instance of type String

- crate is a collection of Rust source code files that you can use it as a dependency
  - To install a crate, you only need to add it under the dependency list in Cargo.toml, then run `cargo build` or `cargo run`
  - `cargo update` install the latest version of crates
