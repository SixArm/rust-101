# Monomorphisation

Rust monomorphization is a process where generic code is transformed into specific code for each concrete type used in the program. In other words, it is the process of generating specialized code for each type that is used in a generic function or struct. 

This is different from traditional dynamic dispatch, where a function or method call is resolved at runtime, based on the type of the object or value being operated on. With monomorphization, the specific implementation of a generic function is determined at compile-time, and there is no runtime overhead associated with dynamic dispatch. 

Overall, monomorphization makes Rust code faster and more efficient than code that relies on dynamic dispatch.

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

In the `main` function, we call add twice: once with integers and once with floats. Since Rust uses monomorphization, the compiler generates two separate versions of the add function, one for integers and one for floats. This results in efficient and optimized code without the overhead of dynamic dispatch.
