# Learn Rust: Zero to Advanced

A comprehensive, self-guided learning path for mastering Rust—from first principles to production-ready systems programming.

## What is Rust?

Rust is a systems programming language that guarantees memory safety and thread safety without a garbage collector. Created by Mozilla Research and now maintained by the Rust Foundation, it delivers the performance of C and C++ with modern language features that prevent entire classes of bugs at compile time.

## Why Rust Matters

**Problems Rust Solves:**

- **Memory Safety Without Garbage Collection**: Eliminates null pointer dereferences, buffer overflows, and use-after-free bugs through its ownership system
- **Fearless Concurrency**: The type system prevents data races, making parallel programming safe and predictable
- **Zero-Cost Abstractions**: High-level features compile down to the same performance as hand-written low-level code
- **Reliable Software**: Catch bugs at compile time rather than in production

**Real-World Impact:**

Rust powers critical infrastructure at Microsoft, Amazon, Google, Discord, Dropbox, and Cloudflare. It's the second language in the Linux kernel, the foundation of new operating systems, and increasingly the choice for performance-critical web services, blockchain infrastructure, and embedded systems.

## Prerequisites

- Basic programming knowledge (variables, functions, control flow)
- Familiarity with command-line interfaces
- Understanding of basic computer science concepts (stack vs heap is helpful but not required)

## Setup

### Install Rust

```bash
# Unix-like systems (macOS, Linux, WSL)
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Windows
# Download and run rustup-init.exe from https://rustup.rs
```

### Verify Installation

```bash
rustc --version
cargo --version
```

### Essential Tools

- **Cargo**: Rust's build tool and package manager (installed with Rust)
- **rust-analyzer**: Language server for IDE integration
- **clippy**: Advanced linter for catching common mistakes
- **rustfmt**: Code formatter

```bash
rustup component add clippy rustfmt
```

### Recommended Editor Setup

- **VS Code**: Install "rust-analyzer" extension
- **IntelliJ/CLion**: Install "Rust" plugin
- **Vim/Neovim**: Use CoC or native LSP with rust-analyzer
- **Helix/Zed**: Built-in Rust support

## Learning Roadmap

### Phase 1: Foundations (2-3 weeks)

**Core Concepts:**

- Variables, mutability, and shadowing
- Data types: scalars and compounds
- Functions and control flow
- Ownership, borrowing, and references
- Slices and string types
- Structs and methods
- Enums and pattern matching
- Error handling with `Result` and `Option`
- Collections: Vec, HashMap, HashSet

**Key Learning:**

The ownership system is Rust's defining feature. Take time to deeply understand:

- Each value has exactly one owner
- Values are dropped when their owner goes out of scope
- Borrowing rules: multiple immutable references OR one mutable reference
- Why these rules prevent data races and memory errors

**Practice Projects:**

- CLI calculator
- Text-based guessing game
- Todo list application (file-based storage)
- Basic file parser (CSV or JSON)

### Phase 2: Intermediate (3-4 weeks)

**Core Concepts:**

- Modules and crate organization
- Generics and type parameters
- Traits and trait bounds
- Lifetimes and lifetime annotations
- Smart pointers: Box, Rc, RefCell, Arc
- Iterators and closures
- Testing and documentation
- Cargo workspaces and dependencies

**Advanced Error Handling:**

- Custom error types
- The `?` operator
- Error propagation patterns
- Third-party crates: `anyhow`, `thiserror`

**Practice Projects:**

- Command-line tool with argument parsing (using `clap`)
- Simple HTTP client (using `reqwest`)
- Data processing pipeline with iterators
- Library crate with comprehensive tests and docs

### Phase 3: Advanced (4-6 weeks)

**Core Concepts:**

- Async/await and futures
- Concurrent programming: threads, channels, synchronization
- Unsafe Rust and FFI
- Macros: declarative and procedural
- Advanced type system features
- Performance optimization and profiling
- Memory layout and representation

**Async Ecosystem:**

- `tokio` or `async-std` runtime
- `futures` crate utilities
- Async traits and patterns
- Dealing with blocking code

**Practice Projects:**

- Async web server (using `axum` or `actix-web`)
- Concurrent data processor
- Simple database or key-value store
- CLI tool with parallel execution

### Phase 4: Specialization (Ongoing)

Choose a domain and go deep:

**Web Development:**

- Backend: `axum`, `actix-web`, `rocket`
- Frontend: `yew`, `leptos`, `dioxus` (WASM)
- GraphQL: `async-graphql`, `juniper`

**Systems Programming:**

- OS development
- Device drivers
- Embedded systems (`embedded-hal`, `embassy`)

**Performance-Critical Applications:**

- Game engines
- Database systems
- Compilers and interpreters

**Blockchain and Cryptography:**

- Smart contracts (`ink!`, Solana)
- Consensus algorithms
- Cryptographic primitives

## Essential Resources

### Official Documentation

- [The Rust Programming Language Book](https://doc.rust-lang.org/book/) - Start here
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/) - Learn by doing
- [The Rustonomicon](https://doc.rust-lang.org/nomicon/) - Unsafe Rust deep dive
- [Async Book](https://rust-lang.github.io/async-book/) - Asynchronous programming
- [Standard Library Docs](https://doc.rust-lang.org/std/) - Comprehensive API reference

### High-Quality Learning Materials

- [Rustlings](https://github.com/rust-lang/rustlings) - Interactive exercises
- [Exercism Rust Track](https://exercism.org/tracks/rust) - Mentored practice
- [Rust Design Patterns](https://rust-unofficial.github.io/patterns/) - Idiomatic code patterns
- [Comprehensive Rust](https://google.github.io/comprehensive-rust/) - Google's 4-day course
- [Too Many Lists](https://rust-unofficial.github.io/too-many-lists/) - Learn through linked list implementations

### Video Content

- [Jon Gjengset's YouTube](https://www.youtube.com/c/JonGjengset) - Advanced Rust concepts
- [Let's Get Rusty](https://www.youtube.com/c/LetsGetRusty) - Book walkthroughs and tutorials

### Community

- [Rust Users Forum](https://users.rust-lang.org/)
- [r/rust](https://reddit.com/r/rust)
- [Rust Discord](https://discord.gg/rust-lang)
- [This Week in Rust](https://this-week-in-rust.org/) - Weekly newsletter

## Project Ideas by Level

### Beginner

- Password generator
- Markdown to HTML converter
- File system organizer
- Simple encryption tool

### Intermediate

- REST API with database
- Chat application (WebSocket)
- Image processing tool
- Package manager clone

### Advanced

- Distributed key-value store
- Programming language interpreter
- Game engine or renderer
- Operating system kernel

## Common Pitfalls and How to Overcome Them

**"Fighting the borrow checker"**: This is normal. The compiler is teaching you to write memory-safe code. Read error messages carefully—they're exceptionally helpful.

**Premature optimization**: Write clear code first. Profile before optimizing. Rust is already fast.

**Overusing `clone()`**: It works, but learn when references and borrowing are the better choice.

**Avoiding lifetimes**: They're not optional in many cases. Understanding them unlocks advanced patterns.

## Measuring Progress

- Can you implement a linked list without fighting the compiler?
- Can you explain when to use `Box<T>` vs `Rc<T>` vs `Arc<T>`?
- Can you write async code that handles errors gracefully?
- Can you read and understand production Rust code?
- Can you contribute to open-source Rust projects?

## Contributing

This is a living document. Contributions, corrections, and suggestions are welcome. Please open an issue or submit a pull request.

## License

This learning guide is released under CC0 (public domain). Learn freely, share widely.

---

**Remember**: Rust has a steep learning curve, but it's a worthwhile investment. The language forces you to think carefully about resource management, concurrency, and error handling—skills that make you a better programmer in any language. Take your time, read compiler errors, and don't skip the fundamentals.

Start with Chapter 1 of [The Book](https://doc.rust-lang.org/book/) and write code every day. You've got this.