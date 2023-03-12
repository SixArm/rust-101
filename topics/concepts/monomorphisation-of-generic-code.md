# Monomorphisation

Rust monomorphization is a process where generic code is transformed into specific code for each concrete type used in the program. In other words, it is the process of generating specialized code for each type that is used in a generic function or struct.

This is different from traditional dynamic dispatch, where a function or method call is resolved at runtime, based on the type of the object or value being operated on. With monomorphization, the specific implementation of a generic function is determined at compile-time, and there is no runtime overhead associated with dynamic dispatch.

Monomorphization in Rust is enabled by the language's support for generics, which allows code to be written once and used with multiple different types. When generic code is compiled, Rust creates specialized copies of the code for each type it is used with, effectively turning the generic code into a collection of concrete, monomorphic functions. This makes Rust code faster and more efficient than code that relies on dynamic dispatch, as there is no need for the program to perform costly runtime lookups to determine which implementation to use.

Overall, Rust's monomorphization allows developers to write generic code that is as fast as hand-written, specific code, without having to duplicate code for each type they want to use it with. This makes Rust a powerful and efficient language for building large-scale applications.

Here's an example of monomorphism in Rust:

```rust
fn add<T: std::ops::Add<Output=T>>(a: T, b: T) -> T {
    a + b
}

fn main() {
    let int_sum = add(1, 2);
    let float_sum = add(1.0, 2.0);

    println!("Integer sum: {}", int_sum);
    println!("Float sum: {}", float_sum);
}
```

In this example, the add function takes two arguments of type `T`, which must implement the `std::ops::Add trait`, and returns their sum of the same type `T`. Because the type parameter `T` is constrained to implement `std::ops::Add`, the compiler can statically determine the concrete type of `T` at compile-time, resulting in monomorphic code that is optimized for the specific types used.

In the main function, we call add twice: once with integers and once with floats. Since Rust uses monomorphization, the compiler generates two separate versions of the add function, one for integers and one for floats. This results in efficient and optimized code without the overhead of dynamic dispatch.
