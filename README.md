# Rust 101

Rust 101 is an introduction to Rust programming, with a focus on topic summaries that we believe can be especially helpful newcomers to Rust and its ecosystem.

Rust 101 aims to explain the topics in a broad way first. We recommend reading Rust 101 along with the official Rust documentation book: [The Rust Programming Language](https://doc.rust-lang.org/book/) by Steve Klabnik and Carol Nichols, with contributions from the Rust Community.

Rust 101 is created by SixArm and Joel Parker Henderson, with content generated by OpenAI ChatGPT using explain prompts.

We welcome constructive feedback, such as topic suggestions, pull requests, etc. We're adding to Rust 101 weekly. You can star this repo if you want to get updates about Rust 101.


## Starters

* [What makes Rust a good programming language?](starters/what-makes-rust-a-good-programming-language.md)

* [What are the hardest parts of Rust?](starters/what-are-the-hardest-parts-of-rust.md)

* [Who might benefit from learning Rust?](starters/who-might-benefit-from-learning-rust.md)


## Comparisons

* [Rust versus C/C++](comparisons/rust-versus-c-cpp.md)

* [Rust versus Java](comparisons/rust-versus-java.md)

* [Rust versus JavaScript](comparisons/rust-versus-javascript.md)

* [Rust versus Python](comparisons/rust-versus-python.md)


## Syntax

* [Annotations for compiler directives](syntax/annotations-for-compiler-directives.md)

* [Destructuring into components](syntax/destructuring-into-components.md)

* [dyn trait for dynamic dispatch](syntax/dyn-trait-for-dynamic-dispatch.md)

* [Enum keyword for enumerations](syntax/enum-keyword-for-enumerations.md)

* [Iterators for traversing collections](syntax/iterators-for-traversing-collections.md)

* [Macros for metaprogramming](syntax/macros-for-metaprogramming.md)

* [Match statement and match arms](syntax/match-statement-and-match-arms.md)

* [Namespaces and mod keyword for modules](syntax/namespaces-and-mod-keyword-for-modules.md)

* [Panic and how to handle it with a hook](syntax/panic-and-how-to-handle-it-with-a-hook.md)

* [Range syntax for a sequence of values](syntax/range-syntax-for-a-sequence-of-values.md)

* [struct keyword for custom data types](syntax/struct-keyword-for-custom-data-types.md)

* [Trait keyword for generic code and polymorphism](syntax/trait-keyword-for-generic-code-and-polymorphism.md)

* [Tuples for ordered collections](syntax/tuples-for-ordered-collections.md)

* What other syntax should we include here?


## Concepts

* [Borrow checker](concepts/borrow-checker.md)

* [Concurrency and parallelism](concepts/concurrency-and-parallelism.md)

* [Channels for communication between threads](concepts/channels-for-communication-between-threads.md)

* [Foreign Function Interface (FFI)](concepts/foreign-function-interface-ffi.md)

* [Futures for asynchronous operations](concepts/futures-for-asynchronous-operations.md)

* [Memory lifetimes](concepts/memory-lifetimes.md)

* [Memory on the stack or the heap](concepts/memory-on-the-stack-or-the-heap.md)

* [Monomorphisation](concepts/monomorphisation-of-generic-code.md)

* [Mutability and immutability](mutability-and-immutability.md)

* [Test framework and test assertions](concepts/test-framework-and-test-assertions.md)

* [Unsafe code](concepts/unsafe-code.md)

* [Zero-cost abstractions](concepts/zero-cost-abstractions.md)

* What other concepts should we include here?


## Traits we use often

* [Debug trait for debugging and printing](traits/debug-trait-for-debugging-and-printing.md)

* [Display trait for formatting](traits/display-trait-for-formatting.md)
  
* [From trait and Into trait for conversions](traits/from-trait-and-into-trait-for-conversions.md)
  
* What other traits should we include here?


## Types we use often

* [Box type for a smart pointer](types/box-smart-pointer.md)

* [Rc (Reference Counted) type for single-thread sharing](types/rc-reference-counted-type-for-single-thread-sharing.md)

* [Arc (Atomically Reference Counted) type for multi-thread sharing](types/arc-atomically-reference-counted-type-for-multi-thread-sharing.md)

* What other types should we include here?


## Tooling we use often

* [rustup command-line tool](tooling/rustup-command-line-tool.md)

* [Cargo package manager and crate packages](tooling/cargo-package-manager-and-crate-packages.md)

* [Clippy linting](tooling/clippy-linting.md)

* [Static analysis for error detection](tooling/static-analysis-for-error-detection.md)

* [Abstract syntax tree (AST)](tooling/abstract-syntax-tree-ast.md)

* [Language Server Protocol (LSP)](tooling/language-server-protocol-lsp.md)

* [cargo-cache crate for caching dependencies](tooling/cargo-cache-crate-for-caching-dependencies.md)

* [cargo-release crate for release automation](tooling/cargo-release-crate-for-release-automation.md)

* What other tooling should we include here?


## Crates we use often

* [Assertables crate for assert macro tests](crates/assertables-crate-for-assert-macro-tests.md)

* [CLAP crate for command line argument parsing](crates/clap-crate-for-command-line-argument-parsing.md)

* [Diesel crate for object-relational mapping](crates/diesel-crate-for-object-relational-mapping.md)

* [itertools crate for extra iterator capabilties](crates/itertools-crate-for-extra-iterator-capabilties.md)

* [Serde crate for serialization and deserialization](crates/serde-crate-for-serialization-and-deserialization.md)

* [sqlx crate for SQL databases](crates/sqlx-crate-for-sql-databases.md)

* [Tokio crate for asynchronous and concurrent code](crates/tokio-crate-for-asynchronous-and-concurrent-code.md)

* What other crates should we include here?
