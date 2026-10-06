# Rust First Step

This repository is the result of following the Udemy course "Master the Rust programming language from A-Z. Includes projects, quizzes, and more. Beginners welcome!" taught by [Boris Paskhaver](https://www.udemy.com/user/borispaskhaver/).

This project represents my first step on the Rust programming journey. It is a simple starting point where I am learning the basics of Rust, getting familiar with the language, and building my foundation for future projects.

## Project

The current project is a minimal Rust application that prints:

```rust
Hello, world!
```

This small example is the classic beginning of a Rust program and marks the start of my learning path.

## Running the project

To run the project locally:

```bash
cargo run
```

## Essential Cargo commands

Cargo is Rust's build tool and package manager. It handles compiling your
project, downloading dependencies, and running tests. Run these commands from
the project directory (the one containing `Cargo.toml`).

### Create a project

Start a new binary application in a new directory:

```bash
cargo new my_app
```

To turn the current directory into a Cargo project instead:

```bash
cargo init
```

Cargo creates a `Cargo.toml` manifest and a `src/main.rs` entry point for a
binary application. Use `cargo new --lib my_library` to create a library
project.

### Check, build, and run

Check for common compilation errors without producing an executable:

```bash
cargo check
```

Compile a debug build:

```bash
cargo build
```

Compile an optimized release build:

```bash
cargo build --release
```

Build and run the application in one step:

```bash
cargo run
```

To pass arguments to your program, put them after `--`:

```bash
cargo run -- arg1 arg2
```

Cargo stores build artifacts in `target/`. Release builds go in
`target/release/`; ordinary debug builds go in `target/debug/`.

### Test, format, and lint

Run the project's tests:

```bash
cargo test
```

Format Rust source files using the standard Rust style:

```bash
cargo fmt
```

Check for common mistakes and suggestions beyond compiler errors:

```bash
cargo clippy
```

`cargo fmt` and `cargo clippy` may require the corresponding Rust components.
You can install them with `rustup component add rustfmt clippy`.

### Documentation and cleanup

Build documentation for your project and its dependencies:

```bash
cargo doc
```

Build and open that documentation in your browser:

```bash
cargo doc --open
```

Remove generated build artifacts:

```bash
cargo clean
```

This removes the `target/` directory; Cargo recreates it the next time you
build the project.

## Essential `rustc` commands

`rustc` is the Rust compiler. Cargo calls it for you when you build or run a
Cargo project. It is useful to know how to call it directly for a standalone
Rust source file, but Cargo is usually the better choice for projects because
it also manages dependencies and project settings.

Check which compiler is installed:

```bash
rustc --version
```

Compile a single source file:

```bash
rustc main.rs
```

This writes an executable in the current directory (`main` on Unix-like
systems, or `main.exe` on Windows). Run that executable directly. To choose
its name and output location, use `-o`:

```bash
rustc main.rs -o my_program
```

For the source file in this repository, a direct compile would be:

```bash
rustc src/main.rs -o hello_world
```

Ask the compiler for an explanation of a specific error code shown in a
diagnostic:

```bash
rustc --explain E0308
```

For this Cargo project, prefer `cargo check`, `cargo build`, or `cargo run`
instead of invoking `rustc` directly.

## Goal

My goal is to continue learning Rust, practice regularly, and grow from this first step into more advanced projects, concepts, and real-world applications.
