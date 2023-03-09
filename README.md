# Rust 101

Rust 101 is an introduction to Rust programming and its ecosystem, with a focus on topics and summaries that can help Rust newcomers.

Rust 101 aims to explain each topic in a broad way. Rust 101 works best along with the official Rust documentation book: [The Rust Programming Language](https://doc.rust-lang.org/book/).

Rust 101 is created by SixArm and Joel Parker Henderson, with content generated by ChatGPT. We welcome constructive feedback, and we're improving this repo often.


## Starters

* [What is a Rust "hello world" program?](topics/starters/what-is-a-rust-hello-world-program.md)

* [What makes Rust a good programming language?](topics/starters/what-makes-rust-a-good-programming-language.md)

* [How does Rust use programming language theory?](topics/starters/how-does-rust-use-programming-language-theory.md)
  
* [What is the Rust ecosystem?](topics/starters/what-is-the-rust-ecosystem.md)

* [Who are Rust leaders?](topics/starters/who-are-rust-leaders.md)


### Learning

* [Who might benefit from learning Rust?](topics/starters/who-might-benefit-from-learning-rust.md)

* [What are good ways to learn Rust?](topics/starters/what-are-good-ways-to-learn-rust.md)

* [What are good open source projects for learning Rust?](topics/starters/what-are-good-open-source-projects-for-learning-rust.md)
  

### Caveats

* [What are the hardest parts of Rust?](topics/starters/what-are-the-hardest-parts-of-rust.md)

* [What is Rust missing?](topics/starters/what-is-rust-missing.md)

* [Why do companies not use Rust?](topics/starters/why-do-companies-not-use-rust.md)


### Comparisons

* [Rust versus C/C++](topics/comparisons/rust-versus-c-cpp.md)

* [Rust versus Go](topics/comparisons/rust-versus-go.md)
  
* [Rust versus Java](topics/comparisons/rust-versus-java.md)

* [Rust versus JavaScript](topics/comparisons/rust-versus-javascript.md)

* [Rust versus Nim](topics/comparisons/rust-versus-nim.md)

* [Rust versus Python](topics/comparisons/rust-versus-python.md)

* [Rust versus Zig](topics/comparisons/rust-versus-zig.md)


### Specialized uses

* [Rust for artificial intelligence and machine learning](topics/uses/rust-for-artificial-intelligence-and-machine-learning.md)
  
* [Rust for embedded devices](topics/uses/rust-for-embedded-devices.md)

* [Rust for game development](topics/uses/rust-for-game-development.md)

* [Rust for graphical user interfaces (GUIs)](topics/users/rust-for-graphical-user-interfaces-guis.md)


## Types & traits & keywords


### Types we use often

* [Scalar types](topics/types/scalar-types.md)
  
* [Compound types](topics/types/compound-types.md)

* [Tuples for ordered collections](topics/syntax/tuples-for-ordered-collections.md)

* [Box type for a smart pointer](topics/types/box-smart-pointer.md)

* [Rc (Reference Counted) type for single-thread sharing](topics/types/rc-reference-counted-type-for-single-thread-sharing.md)

* [Arc (Atomically Reference Counted) type for multi-thread sharing](topics/types/arc-atomically-reference-counted-type-for-multi-thread-sharing.md)


### Traits we use often

* [Copy trait and Clone trait for duplicating values](topics/traits/copy-trait-and-clone-trait-for-duplication.md)

* [Debug trait for debugging and printing](topics/traits/debug-trait-for-debugging-and-printing.md)

* [Display trait for formatting](topics/traits/display-trait-for-formatting.md)
  
* [dyn trait for dynamic dispatch](topics/traits/dyn-trait-for-dynamic-dispatch.md)

* [Eq, PartialEq, Ord, PartialOrd, Hash traits for comparisons](topics/traits/eq-partialeq-ord-partialord-hash-traits-for-comparisons.md)
  
* [From trait and Into trait for conversions](topics/traits/from-trait-and-into-trait-for-conversions.md)


### Keywords we use often

* [async/await keywords for asynchronous code](topics/keywords/async-await-keywords-for-asynchronous-code.md)

* [enum keyword for enumerations](topics/keywords/enum-keyword-for-enumerations.md)

* [match keyword and match arms for control flow](topics/keywords/match-keyword-and-match-arms-for-control-flow.md)

* [mod keyword for modules and namespaces](topics/keywords/mod-keyword-for-modules-and-namespaces.md)

* [struct keyword for custom data types](topics/keywords/struct-keyword-for-custom-data-types.md)

* [trait keyword for generic code and polymorphism](topics/keywords/trait-keyword-for-generic-code-and-polymorphism.md)


## Coding


### Syntax

* [Annotations for compiler directives](topics/syntax/annotations-for-compiler-directives.md)

* [Destructuring into components](topics/syntax/destructuring-into-components.md)

* [Iterators for traversing collections](topics/syntax/iterators-for-traversing-collections.md)

* [Closures for anonymous functions](topics/syntax/closures-for-anonymous-functions.md)
  
* [Macros for metaprogramming](topics/syntax/macros-for-metaprogramming.md)

* [Panic and how to handle it with a hook](topics/syntax/panic-and-how-to-handle-it-with-a-hook.md)

* [Range syntax for a sequence of values](topics/syntax/range-syntax-for-a-sequence-of-values.md)


### Memory

* [Memory lifetimes](topics/concepts/memory-lifetimes.md)

* [Memory on the stack or the heap](topics/concepts/memory-on-the-stack-or-the-heap.md)

* [Memory ownership and borrowing](topics/concepts/memory-ownership-and-borrowing.md)

* [Mutability and immutability](topics/mutability-and-immutability.md)


### Concepts

* [Borrow checker](topics/concepts/borrow-checker.md)
  
* [Concurrency and parallelism](topics/concepts/concurrency-and-parallelism.md)

* [Channels for communication between threads](topics/concepts/channels-for-communication-between-threads.md)

* [Dependency injection (DI) to reduce coupling](topics/concepts/dependency-injection-di-to-reduce-coupling.md)

* [Design patterns](topics/concepts/design-patterns.rs)
  
* [Error messages](topics/concepts/error-messages.md)
  
* [Foreign Function Interface (FFI)](topics/concepts/foreign-function-interface-ffi.md)

* [Futures for asynchronous operations](topics/concepts/futures-for-asynchronous-operations.md)

* [Model-view-controller (MVC)](topics/concepts/model-view-controller-mvc.md)

* [Monomorphisation](topics/concepts/monomorphisation-of-generic-code.md)

* [Procedural programming versus functional programming](topics/concepts/procedural-programming-versus-functional-programming.md)

* [Resource Acquisition Is Initialization (RAII)](topics/concepts/resource-acquisition-is-initialization.md)

* [SOLID principles for software design](topics/concepts/solid-principles-for-software-design.md)

* [Test framework and test assertions](topics/concepts/test-framework-and-test-assertions.md)

* [Unsafe code](topics/concepts/unsafe-code.md)

* [WebAssembly (WASM)](topics/concepts/webassembly-wasm.md)

* [Zero-cost abstractions](topics/concepts/zero-cost-abstractions.md)


## Tooling


### Tooling we use often

* [rustup command-line tool](topics/tooling/rustup-command-line-tool.md)

* [Cargo package manager and crate packages](topics/tooling/cargo-package-manager-and-crate-packages.md)

* [Clippy linting](topics/tooling/clippy-linting.md)

* [Cross-compiling for multiple platforms](topics/tooling/cross-compiling-for-multiple-platforms.md)


### Tooling concepts

* [Abstract syntax tree (AST)](topics/tooling/abstract-syntax-tree-ast.md)

* [Tree-sitter parsing library](topics/tooling/tree-sitter-parsing-library.md)
  
* [Language Server Protocol (LSP)](topics/tooling/language-server-protocol-lsp.md)

* [Static analysis for error detection](topics/tooling/static-analysis-for-error-detection.md)


## Crates


### Crates we like for many of our programs

* [Assertables crate for assert macro tests](topics/crates/assertables-crate-for-assert-macro-tests.md)

* [itertools crate for extra iterator capabilties](topics/crates/itertools-crate-for-extra-iterator-capabilties.md)

* [log crate for logging messages](topics/crates/log-crate-for-logging-messages.md)

* [once_cell crate for lazy global variables](topics/crates/once-cell-crate-for-lazy-global-variables.md)
 
* [regex crate for regular expressions](topics/crates/regex-crate-for-regular-expressions.md)
  
* [reqwest crate for HTTP requests](topics/reqwest-crate-for-http-requests.md)

* [Serde crate for serialization and deserialization](topics/crates/serde-crate-for-serialization-and-deserialization.md)


### Crates we like for text-based user interfaces

* [CLAP crate for command line argument parsing](topics/crates/clap-crate-for-command-line-argument-parsing.md)

* [Cursive crate for text-based user interfaces](topics/crates/cursive-crate-for-text-based-user-interfaces.md)
  
* [Textwrap crate for text wrapping](topics/crates/textwra-crate-for-text-wrapping.md)


### Crates we like for cargo workflows

* [cargo-cache crate for caching dependencies](topics/crates/cargo-cache-crate-for-caching-dependencies.md)

* [cargo-dist crate for distribution archives](topics/crates/cargo-dist-crate-for-distribution-archives.md)

* [cargo-release crate for release automation](topics/crates/cargo-release-crate-for-release-automation.md)


### Crates we like for data analysis

* [arrow-csv crate for parsing CSV data to Arrow data](topics/crates/arrow-csv-crate-for-parsing-csv-data-to-arrow-data.md)

* [CSV crate for comma-separated values](topics/crates/csv-crate-for-comma-separated-values.md)

* [Polars crate for data analysis](topics/crates/polars-crate-for-data-analysis.md)


### Crates we like for database access

* [Diesel crate for object-relational mapping](topics/crates/diesel-crate-for-object-relational-mapping.md)

* [Rusqlite crate for SQLite databases](topics/crates/rusqlite-crate-for-sqlite-databases.md)

* [sqlx crate for SQL databases](topics/crates/sqlx-crate-for-sql-databases.md)


### Crates we like for web services

* [axum crate for web services](topics/crates/axum-crate-for-web-services.md)

* [Hyper crate for HTTP clients/servers](topics/crates/hyper-crate-for-http-clients-servers.md)
  
* [Tokio crate for asynchronous and concurrent code](topics/crates/tokio-crate-for-asynchronous-and-concurrent-code.md)

