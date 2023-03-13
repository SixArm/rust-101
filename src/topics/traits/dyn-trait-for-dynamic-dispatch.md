# dyn trait for dynamic dispatch

In Rust, a `dyn trait` is a way to specify a trait object with dynamic dispatch.

A `trait` object is a pointer to an object that implements a trait, and is used when the concrete type of an object is not known at compile time. In other words, it allows you to write code that can work with different types that implement a particular trait without knowing the exact type at compile time.

When defining a `trait` object in Rust, you can use the `dyn` keyword to indicate that the trait object should be dynamically dispatched. This means that the specific implementation of the trait for a given object will be determined at runtime rather than at compile time.

For example, consider the following trait definition:

```rust
trait MyTrait {
    fn my_method(&self);
}
```

To define a trait object with dynamic dispatch, you can use the dyn keyword as follows:

```rust
fn my_function(obj: &dyn MyTrait) {
    obj.my_method();
}
```

In this example, `my_function` takes a reference to a trait object that implements the `MyTrait` trait, with dynamic dispatch specified using the `dyn` keyword. This means that at runtime, the specific implementation of `my_method` for the given object will be determined dynamically.

Using `dyn trait` allows Rust to provide runtime polymorphism, which is useful in situations where the concrete type of an object is not known at compile time, but needs to be determined at runtime. However, it can come at a performance cost compared to static dispatch, which is resolved at compile time.
