# Rhai script

Rhai is an embedded scripting language for Rust that is designed to be easy to use and integrate with Rust applications. Rhai is a dynamically typed language with support for high-level data types such as arrays, maps, and functions. It also supports Rust-style ownership and borrowing, making it easy to integrate with Rust's memory management system.

One of the key features of Rhai is its safety and security. Rhai enforces sandboxing by default, which means that scripts executed within a Rhai interpreter cannot access or modify the host environment. Rhai also supports a variety of security features such as timeouts, memory limits, and access controls to ensure that scripts cannot cause harm to the host application.

Rhai's syntax is similar to Rust's syntax, making it easy for Rust developers to learn and use. Rhai also provides a number of built-in functions and operators that simplify common scripting tasks such as string manipulation, math operations, and control flow.

Overall, Rhai is a powerful and safe scripting language that is well-suited for Rust applications. Its ease of use and security features make it a great choice for developers who want to add scripting capabilities to their Rust applications.

Here is an example of using Rust as an embedded language in Rhai script to perform arithmetic operations:

```rust
use rhai::{Engine, EvalAltResult};

fn main() -> Result<(), Box<dyn std::error::Error>> {
    let mut engine = Engine::new();
    
    let result = engine.eval::<i32>("2 + 2")?;
    println!("2 + 2 = {}", result); // should print 4
    
    let result = engine.eval::<f64>("3.14 * 2.0")?;
    println!("3.14 * 2.0 = {}", result); // should print 6.28
    
    let result = engine.eval::<i32>("10 / 3")?;
    println!("10 / 3 = {}", result); // should print 3
    
    Ok(())
}
```

In this example, the Rhai script is used to evaluate arithmetic expressions, while Rust is used as an embedded language to perform the actual calculations. This allows for the use of Rust's strong typing and performance while still being able to execute dynamic code using Rhai.
