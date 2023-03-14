# Rust Programmer Guidebook (RPG)

The Rust Programmer Guidebook (RPG) covers hundreds of topics about the Rust Programmer language and its ecosystem. The focus is on topics and summaries that can help developers learn Rust, understand it, and use it professionally.

The Rust Programmer Guidebook aims to explain each topic in a broad way, so that any developer can read any topic, in any order, any time. This style works best along with the official Rust book: [The Rust Programming Language](https://doc.rust-lang.org/book/).

The Rust Programmer Guidebook is by SixArm Software and Joel Parker Henderson, with topic content generated by ChatGPT. We welcome constructive feedback, and all ideas for improvement. We update this repo frequently with new topics and new examples.

IMPORTANT: THIS IS VERSION 0.5. THIS IS A DRAFT WORK IN PROGRESS. THIS VERSION IS NOT INTENDED FOR PUBLICATION.

<https://github.com/sixarm/rust-programmer-guidebook>


## Starters

* [What is a Rust "hello world" program?](src/topics/starters/what-is-a-rust-hello-world-program.md)

* [What is a Rust "FizzBuzz" program?](src/topics/starters/what-is-a-rust-fizzbuzz-program.md)

* [What makes Rust good?](src/topics/starters/what-makes-rust-good.md)

* [Is programming language theory in Rust?](src/topics/starters/is-programming-language-theory-in-rust.md)
  
* [What is the Rust ecosystem?](src/topics/starters/what-is-the-rust-ecosystem.md)

* [Who are Rust leaders?](src/topics/starters/who-are-rust-leaders.md)


### Learning

* [Who might benefit from learning Rust?](src/topics/starters/who-might-benefit-from-learning-rust.md)

* [What are good ways to learn Rust?](src/topics/starters/what-are-good-ways-to-learn-rust.md)

* [What are good projects to learn Rust?](src/topics/starters/what-are-good-projects-to-learn-rust.md)
  

### Caveats

* [What are the hardest parts of Rust?](src/topics/starters/what-are-the-hardest-parts-of-rust.md)

* [What is Rust missing?](src/topics/starters/what-is-rust-missing.md)

* [Why do companies not use Rust?](src/topics/starters/why-do-companies-not-use-rust.md)


## Rust in context


### What makes Rust special?

* [Borrow checker](src/topics/concepts/borrow-checker.md)
  
* [Channels for thread communication](src/topics/concepts/channels-for-thread-communication.md)

* [Concurrency and parallelism](src/topics/concepts/concurrency-and-parallelism.md)

* [Error messages](src/topics/concepts/error-messages.md)
  
* [Foreign Function Interface (FFI)](src/topics/concepts/foreign-function-interface-ffi.md)

* [Futures for asynchronous operations](src/topics/concepts/futures-for-asynchronous-operations.md)

* [Monomorphisation](src/topics/concepts/monomorphisation-of-generic-code.md)

* [Rust stable versus Rust nightly](src/topics/concepts/rust-stable-versus-rust-nightly.md)

* [Unsafe code](src/topics/concepts/unsafe-code.md)

* [WebAssembly (WASM)](src/topics/concepts/webassembly-wasm.md)

* [Zero-cost abstractions](src/topics/concepts/zero-cost-abstractions.md)


### Comparisons

* [Rust versus C/C++](src/topics/comparisons/rust-versus-c-cpp.md)

* [Rust versus Go](src/topics/comparisons/rust-versus-go.md)
  
* [Rust versus Java](src/topics/comparisons/rust-versus-java.md)

* [Rust versus JavaScript](src/topics/comparisons/rust-versus-javascript.md)

* [Rust versus Nim](src/topics/comparisons/rust-versus-nim.md)

* [Rust versus Python](src/topics/comparisons/rust-versus-python.md)

* [Rust versus Zig](src/topics/comparisons/rust-versus-zig.md)


### Specialized uses

* [Rust for artificial intelligence](src/topics/uses/rust-for-artificial-intelligence.md)

* [Rust for financial technology (fintech)](src/topics/uses/rust-for-financial-technology-fintech.md)

* [Rust for embedded devices](src/topics/uses/rust-for-embedded-devices.md)

* [Rust for game development](src/topics/uses/rust-for-game-development.md)

* [Rust for graphical user interfaces (GUIs)](src/topics/uses/rust-for-graphical-user-interfaces-guis.md)

* [Rust for Linux drivers](src/topics/uses/rust-for-linux-drivers.md)


## Types & traits & keywords


### Types we use often

* [Scalar types](src/topics/types/scalar-types.md)
  
* [Compound types](src/topics/types/compound-types.md)

* [Tuples for ordered collections](src/topics/syntax/tuples-for-ordered-collections.md)


### Types we use often for memory areas

* [Box type for a smart pointer](src/topics/types/box-smart-pointer.md)

* [Rc type for single-thread sharing](src/topics/types/rc-type-for-single-thread-sharing.md)

* [Arc type for multi-thread sharing](src/topics/types/arc-type-for-multi-thread-sharing.md)

* [Pin type for memory location](src/topics/types/pin-type-for-memory-location.md)


### Traits we use often

* [Copy trait and Clone trait for duplicating values](src/topics/traits/copy-trait-and-clone-trait-for-duplication.md)

* [Debug trait for debugging and printing](src/topics/traits/debug-trait-for-debugging-and-printing.md)

* [Display trait for formatting](src/topics/traits/display-trait-for-formatting.md)
  
* [dyn trait for dynamic dispatch](src/topics/traits/dyn-trait-for-dynamic-dispatch.md)

* [Eq, PartialEq, Ord, PartialOrd, Hash traits](src/topics/traits/eq-partialeq-ord-partialord-hash-traits.md)
  
* [From and Into traits for conversions](src/topics/traits/from-and-into-traits-for-conversions.md)

* [Send and Sync traits for multithreading](src/topics/traits/send-and-sync-traits-for-multithreading.md)


### Keywords we use often

* [async/await keywords for asynchronicity](src/topics/keywords/async-await-keywords-for-asynchronicity.md)

* [enum keyword for enumerations](src/topics/keywords/enum-keyword-for-enumerations.md)

* [match keyword for control flow](src/topics/keywords/match-keyword-for-control-flow.md)

* [mod keyword for module namespaces](src/topics/keywords/mod-keyword-for-module-namespaces.md)

* [struct keyword for custom data types](src/topics/keywords/struct-keyword-for-custom-data-types.md)

* [trait keyword for polymorphism](src/topics/keywords/trait-keyword-for-polymorphism.md)


### Macros we use often

* [catch_unwind! macro for handling panic](src/topics/macros/catch-unwind-macro-to-handle-panic.md)

* [macro_rules! macro for declarative macros](src/topics/macros/macro-rules-for-declarative-macros.md)


## Coding


### Syntax

* [Annotations for compiler directives](src/topics/syntax/annotations-for-compiler-directives.md)

* [Destructuring into components](src/topics/syntax/destructuring-into-components.md)

* [Iterators for traversing collections](src/topics/syntax/iterators-for-traversing-collections.md)

* [Closures for anonymous functions](src/topics/syntax/closures-for-anonymous-functions.md)
  
* [Macros for metaprogramming](src/topics/syntax/macros-for-metaprogramming.md)

* [Panic and how to handle it with a hook](src/topics/syntax/panic-and-how-to-handle-it-with-a-hook.md)

* [Range syntax for a sequence of values](src/topics/syntax/range-syntax-for-a-sequence-of-values.md)


### Memory

* [Memory lifetimes](src/topics/concepts/memory-lifetimes.md)

* [Memory on the stack or the heap](src/topics/concepts/memory-on-the-stack-or-the-heap.md)

* [Memory ownership and borrowing](src/topics/concepts/memory-ownership-and-borrowing.md)

* [Mutability and immutability](src/topics/concepts/mutability-and-immutability.md)


### Testing

* [Test framework and test assertions](src/topics/testing/test-framework-and-test-assertions.md)

* [Unit testing](src/topics/testing/unit-testing.md)

* [Integration testing](src/topics/testing/integration-testing.md)

* [Documentation testing](src/topics/testing/documentation-testing.md)

* [Source-based coverage](src/topics/testing/source-based-coverage.md)

* [Test-driven development (TDD)](src/topics/testing/test-driven-development-tdd.md)


### Examples

* [Access a database with rusqlite](src/topics/examples/acccess-a-database-with-rusqlite.md)
  
* [List directories recursively with walkdir](src/topics/examples/list-directories-recursively-with-walkdir.md)
  
* [Make HTTP GET request with reqwest](src/topics/examples/make-http-get-request-with-reqwest.md)

* [Parse JSON data with Serde](src/topics/examples/parse-json-data-with-serde.md)

* [Read a spreadsheet with CSV](src/topics/examples/read-a-spreadsheet-with-csv.md)

* [Run a terminal program with cursive](src/topics/examples/run-a-terminal-program-with-cursive.md)

* [Search a text file with regex](src/topics/examples/search-a-text-file-with-regex.md)

 
## Tooling & tactics


### Tooling we use often

* [rustup command-line tool](src/topics/tooling/rustup-command-line-tool.md)

* [Cargo package manager and crates](src/topics/tooling/cargo-package-manager-and-crates.md)

* [Clippy linting](src/topics/tooling/clippy-linting.md)

* [Rustfmt for code formatting](src/topics/tooling/rustfmt-for-code-formatting.md)

* [Rust mdBook for documentation](src/topics/tooling/rust-mdbook-for-documentation.md)

* [Cross-compiling for multiple platforms](src/topics/tooling/cross-compiling-for-multiple-platforms.md)

* [Rhai script](src/topics/tooling/rhai-script.md)


### Tooling concepts

* [Abstract syntax tree (AST)](src/topics/tooling/abstract-syntax-tree-ast.md)

* [Tree-sitter parsing library](src/topics/tooling/tree-sitter-parsing-library.md)
  
* [Language Server Protocol (LSP)](src/topics/tooling/language-server-protocol-lsp.md)

* [Static analysis for error detection](src/topics/tooling/static-analysis-for-error-detection.md)


### Tactics, patterns, idioms, and paradigms

* [Architecture decision record (ADR)](src/topics/concepts/architecture-decision-record-adr.md)

* [Design patterns](src/topics/concepts/design-patterns.md)

* [Dependency injection (DI)](src/topics/concepts/dependency-injection-di.md)

* [Domain-driven design (DDD)](src/topics/concepts/domain-driven-design-ddd.md)
  
* [Model-view-controller (MVC)](src/topics/concepts/model-view-controller-mvc.md)

* [Object-oriented versus functional](src/topics/concepts/object-oriented-versus-functional.md)

* [Procedural versus functional](src/topics/concepts/procedural-versus-functional.md)

* [Resource Acquisition Is Initialization (RAII)](src/topics/concepts/resource-acquisition-is-initialization.md)

* [SOLID principles for software design](src/topics/concepts/solid-principles-for-software-design.md)

* [The Law of Demeter](src/topics/concepts/the-law-of-demeter.md)
  

## Crates


### Crates we like for many of our programs

* [Assertables crate for assert macro tests](src/topics/crates/assertables-crate-for-assert-macro-tests.md)

* [log crate for logging messages](src/topics/crates/log-crate-for-logging-messages.md)

* [once_cell crate for lazy global variables](src/topics/crates/once-cell-crate-for-lazy-global-variables.md)
 
* [regex crate for regular expressions](src/topics/crates/regex-crate-for-regular-expressions.md)
  
* [Serde crate for serialize/deserialize](src/topics/crates/serde-crate-for-serialize-deserialize.md)

* [walkdir crate for traversing directories](src/topics/crates/walkdir-crate-for-traversing-directories.md)
  

### Crates we like for text-based interfaces

* [CLAP crate for command line arg parsing](src/topics/crates/clap-crate-for-command-line-arg-parsing.md)

* [Cursive crate for terminal user interfaces](src/topics/crates/cursive-crate-for-terminal-user-interfaces.md)
  
* [Textwrap crate for text wrapping](src/topics/crates/textwrap-crate-for-text-wrapping.md)


### Crates we like for cargo workflows

* [cargo-cache crate for caching builds](src/topics/crates/cargo-cache-crate-for-caching-builds.md)

* [cargo-dist crate for distribution archives](src/topics/crates/cargo-dist-crate-for-distribution-archives.md)

* [cargo-release crate for release automation](src/topics/crates/cargo-release-crate-for-release-automation.md)

* [cargo-make crate for task runners](src/topics/crates/cargo-make-crate-for-task-runners.md)
  

### Crates we like for concurrency and parallelism

* [Crossbeam crate for concurrency](src/topics/crates/crossbeam-crate-for-concurrency.md)

* [itertools crate for iterator extras](src/topics/crates/itertools-crate-for-iterator-extras.md)

* [parking_lot crate for synchronization](src/topics/crates/parking-lot-crate-for-syncroniziation.md)

* [Rayon crate for parallelism](src/topics/crates/rayon-crate-for-parallelism.md)


### Crates we like for data analysis

* [arrow-csv crate for loading CSV to Arrow](src/topics/crates/arrow-csv-crate-for-loading-csv-to-arrow.md)

* [CSV crate for comma-separated values](src/topics/crates/csv-crate-for-comma-separated-values.md)

* [Polars crate for data analysis](src/topics/crates/polars-crate-for-data-analysis.md)


### Crates we like for database access

* [Diesel crate for object-relational mapping](src/topics/crates/diesel-crate-for-object-relational-mapping.md)

* [Rusqlite crate for SQLite databases](src/topics/crates/rusqlite-crate-for-sqlite-databases.md)

* [sqlx crate for SQL databases](src/topics/crates/sqlx-crate-for-sql-databases.md)


### Crates we like for web services

* [axum crate for web services](src/topics/crates/axum-crate-for-web-services.md)

* [Hyper crate for HTTP clients/servers](src/topics/crates/hyper-crate-for-http-clients-servers.md)

* [prost crate for protocol buffers](src/topics/crates/prost-crate-for-protocol-buffers.md)

* [reqwest crate for HTTP requests](src/topics/crates/reqwest-crate-for-http-requests.md)

* [Tokio crate for asynchronicity/concurrency](src/topics/crates/tokio-crate-for-asynchronicity-concurrency.md)

* [tonic crate for gRPC](src/topics/crates/tonic-crate-for-grpc.rs)
