# Rust 101

Rust 101 is an introduction to Rust programming and its ecosystem, with a focus on topic summaries that can help Rust newcomers.

Rust 101 aims to explain each topic in a broad way. Rust 101 works best along with the official Rust documentation book: [The Rust Programming Language](https://doc.rust-lang.org/book/).

Rust 101 is created by SixArm and Joel Parker Henderson, with content generated by OpenAI ChatGPT using explain prompts. We welcome constructive feedback, and we're improving this repo often.


## Starters

* [What makes Rust a good programming language?](starters/what-makes-rust-a-good-programming-language.md)

* [What is the Rust ecosystem?](starters/what-is-the-rust-ecosystem.md)
  
* [What is a Rust "hello world" program?](starters/what-is-a-rust-hello-world-program.md)

* [Who might benefit from learning Rust?](starters/who-might-benefit-from-learning-rust.md)

* [What are good ways to learn Rust?](starters/what-are-good-ways-to-learn-rust.md)

* [Who are Rust leaders?](starters/who-are-rust-leaders.md)
  

### Caveats

* [What are the hardest parts of Rust?](starters/what-are-the-hardest-parts-of-rust.md)

* [What is Rust missing?](starters/what-is-rust-missing.md)

* [Why do companies not use Rust?](starters/why-do-companies-not-use-rust.md)


### Comparisons

* [Rust versus C/C++](comparisons/rust-versus-c-cpp.md)

* [Rust versus Go](comparisons/rust-versus-go.md)
  
* [Rust versus Java](comparisons/rust-versus-java.md)

* [Rust versus JavaScript](comparisons/rust-versus-javascript.md)

* [Rust versus Python](comparisons/rust-versus-python.md)


### Specialized uses

* [Rust for artificial intelligence and machine learning](uses/rust-for-artificial-intelligence-and-machine-learning.md)
  
* [Rust for embedded devices](uses/rust-for-embedded-devices.md)

* [Rust for game development](uses/rust-for-game-development.md)

* [Rust for graphical user interfaces (GUIs)](users/rust-for-graphical-user-interfaces-guis.md)


## Types & traits & keywords


### Types we use often

* [Scalar types](types/scalar-types.md)
  
* [Compound types](types/compound-types.md)

* [Tuples for ordered collections](syntax/tuples-for-ordered-collections.md)

* [Box type for a smart pointer](types/box-smart-pointer.md)

* [Rc (Reference Counted) type for single-thread sharing](types/rc-reference-counted-type-for-single-thread-sharing.md)

* [Arc (Atomically Reference Counted) type for multi-thread sharing](types/arc-atomically-reference-counted-type-for-multi-thread-sharing.md)


### Traits we use often

* [Copy trait and Clone trait for duplicating values](traits/copy-trait-and-clone-trait-for-duplication.md)

* [Debug trait for debugging and printing](traits/debug-trait-for-debugging-and-printing.md)

* [Display trait for formatting](traits/display-trait-for-formatting.md)
  
* [dyn trait for dynamic dispatch](traits/dyn-trait-for-dynamic-dispatch.md)

* [Eq, PartialEq, Ord, PartialOrd, Hash traits for comparisons](traits/eq-partialeq-ord-partialord-hash-traits-for-comparisons.md)
  
* [From trait and Into trait for conversions](traits/from-trait-and-into-trait-for-conversions.md)


### Keywords we use often

* [async/await keywords for asynchronous code](keywords/async-await-keywords-for-asynchronous-code.md)

* [enum keyword for enumerations](keywords/enum-keyword-for-enumerations.md)

* [match keyword and match arms for control flow](keywords/match-keyword-and-match-arms-for-control-flow.md)

* [mod keyword for modules and namespaces](keywords/mod-keyword-for-modules-and-namespaces.md)

* [struct keyword for custom data types](keywords/struct-keyword-for-custom-data-types.md)

* [trait keyword for generic code and polymorphism](keywords/trait-keyword-for-generic-code-and-polymorphism.md)


## Coding


### Syntax

* [Annotations for compiler directives](syntax/annotations-for-compiler-directives.md)

* [Destructuring into components](syntax/destructuring-into-components.md)

* [Iterators for traversing collections](syntax/iterators-for-traversing-collections.md)

* [Closures for anonymous functions](syntax/closures-for-anonymous-functions.md)
  
* [Macros for metaprogramming](syntax/macros-for-metaprogramming.md)

* [Panic and how to handle it with a hook](syntax/panic-and-how-to-handle-it-with-a-hook.md)

* [Range syntax for a sequence of values](syntax/range-syntax-for-a-sequence-of-values.md)


### Memory

* [Memory lifetimes](concepts/memory-lifetimes.md)

* [Memory on the stack or the heap](concepts/memory-on-the-stack-or-the-heap.md)

* [Memory ownership and borrowing](concepts/memory-ownership-and-borrowing.md)

* [Mutability and immutability](mutability-and-immutability.md)


### Concepts

* [Borrow checker](concepts/borrow-checker.md)
  
* [Concurrency and parallelism](concepts/concurrency-and-parallelism.md)

* [Channels for communication between threads](concepts/channels-for-communication-between-threads.md)

* [Dependency injection (DI) to reduce coupling](concepts/dependency-injection-di-to-reduce-coupling.md)

* [Design patterns](concepts/design-patterns.rs)
  
* [Error messages](concepts/error-messages.md)
  
* [Foreign Function Interface (FFI)](concepts/foreign-function-interface-ffi.md)

* [Futures for asynchronous operations](concepts/futures-for-asynchronous-operations.md)

* [Monomorphisation](concepts/monomorphisation-of-generic-code.md)

* [Procedural programming versus functional programming](concepts/procedural-programming-versus-functional-programming.md)

* [Resource Acquisition Is Initialization (RAII)](concepts/resource-acquisition-is-initialization.md)

* [Test framework and test assertions](concepts/test-framework-and-test-assertions.md)

* [Unsafe code](concepts/unsafe-code.md)

* [WebAssembly (WASM)](concepts/webassembly-wasm.md)

* [Zero-cost abstractions](concepts/zero-cost-abstractions.md)


## Tooling


### Tooling we use often

* [rustup command-line tool](tooling/rustup-command-line-tool.md)

* [Cargo package manager and crate packages](tooling/cargo-package-manager-and-crate-packages.md)

* [Clippy linting](tooling/clippy-linting.md)

* [Cross-compiling for multiple platforms](tooling/cross-compiling-for-multiple-platforms.md)


### Tooling concepts

* [Abstract syntax tree (AST)](tooling/abstract-syntax-tree-ast.md)

* [Tree-sitter parsing library](tooling/tree-sitter-parsing-library.md)
  
* [Language Server Protocol (LSP)](tooling/language-server-protocol-lsp.md)

* [Static analysis for error detection](tooling/static-analysis-for-error-detection.md)


## Crates


### Crates we like for many of our programs

* [Assertables crate for assert macro tests](crates/assertables-crate-for-assert-macro-tests.md)

* [itertools crate for extra iterator capabilties](crates/itertools-crate-for-extra-iterator-capabilties.md)

* [log crate for logging messages](crates/log-crate-for-logging-messages.md)

* [reqwest crate for HTTP requests](reqwest-crate-for-http-requests.md)

* [Serde crate for serialization and deserialization](crates/serde-crate-for-serialization-and-deserialization.md)


### Crates we like for text-based user interfaces

* [CLAP crate for command line argument parsing](crates/clap-crate-for-command-line-argument-parsing.md)

* [Cursive crate for text-based user interfaces](crates/cursive-crate-for-text-based-user-interfaces.md)
  
* [Textwrap crate for text wrapping](crates/textwra-crate-for-text-wrapping.md)


### Crates we like for cargo workflows

* [cargo-cache crate for caching dependencies](crates/cargo-cache-crate-for-caching-dependencies.md)

* [cargo-dist crate for distribution archives](crates/cargo-dist-crate-for-distribution-archives.md)

* [cargo-release crate for release automation](crates/cargo-release-crate-for-release-automation.md)


### Crates we like for database access

* [Diesel crate for object-relational mapping](crates/diesel-crate-for-object-relational-mapping.md)

* [Rusqlite crate for SQLite databases](crates/rusqlite-crate-for-sqlite-databases.md)

* [sqlx crate for SQL databases](crates/sqlx-crate-for-sql-databases.md)


### Crates we like for web services

* [axum crate for web services](crates/axum-crate-for-web-services.md)

* [Hyper crate for HTTP clients/servers](crates/hyper-crate-for-http-clients-servers.md)
  
* [Tokio crate for asynchronous and concurrent code](crates/tokio-crate-for-asynchronous-and-concurrent-code.md)

