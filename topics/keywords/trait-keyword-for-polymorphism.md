# Trait keyword for polymorphism

In Rust, a trait is a language construct that defines a set of methods that can be implemented by a type. Traits allow Rust to achieve polymorphism and code reuse without sacrificing performance or safety.

A trait is defined using the `trait` keyword, followed by the name of the trait and a list of method signatures:

```rust
trait MyTrait {
    fn method1(&self);
    fn method2(&mut self, value: i32) -> i32;
}
```

This defines a trait called `MyTrait` with two methods, `method1` and `method2`. The methods have different signatures and can have different behavior for each type that implements the trait.

To implement a trait for a type, you use the `impl` keyword followed by the trait name and the implementation block:

```rust
struct MyStruct;

impl MyTrait for MyStruct {
    fn method1(&self) {
        println!("Hello from method1!");
    }
    fn method2(&mut self, value: i32) -> i32 {
        value * 2
    }
}
```

This defines an implementation of `MyTrait` for the `MyStruct` type. The `method1` method simply prints a message to the console, while `method2` takes a mutable reference to self and returns the input value multiplied by two.

Once a trait is implemented for a type, any function that takes the trait as a parameter can use the implemented methods:

```rust
fn use_trait<T: MyTrait>(item: &mut T) {
    item.method1();
    let result = item.method2(10);
    println!("method2 returned {}", result);
}
```

This function takes a mutable reference to any type that implements `MyTrait`, calls `method1` and `method2` on it, and prints the result of `method2` to the console.

Traits can also be used for generic programming and code reuse. For example, Rust's standard library defines many traits, such as Iterator, Clone, and Debug, that can be implemented by custom types to provide functionality that's common across many different types.
