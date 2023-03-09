# What is a Rust "hello world" program?

In Rust, a simple "Hello, world!" program is:

```rust
fn main() {
    println!("Hello, world!");
}
```

This program contains a single function, `main()`, which is the entry point for the program. The function body is enclosed in curly braces `{}` and contains a single statement:

```rust
println!("Hello, world!");
```

This statement prints the text "Hello, world!" to the console using Rust's standard library macro `println!()`. The `println!()` macro is a convenient way to print formatted text to the console, and in this case, it simply prints the string literal "Hello, world!".

When you run this program, you should see the text "Hello, world!" printed to the console.