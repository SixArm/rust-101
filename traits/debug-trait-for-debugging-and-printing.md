# Debug trait for debugging and printing

In Rust, the `Debug` trait is a built-in trait that allows developers to print and debug Rust types. It is used to provide a basic representation of a type suitable for debugging purposes.

When a type implements the `Debug` trait, it can be printed using the println! macro with the `{:?}` format specifier. This will print a debug representation of the type, which is often more informative than the default string representation.

To implement the `Debug` trait for a custom type, developers need to define a `debug` method on the type that returns a `fmt::Debug` trait object. This method should return a formatter that describes the structure of the type in a way that is suitable for debugging.

For example, let's consider a simple `Point` struct:

```rust
#[derive(Debug)]
struct Point {
    x: i32,
    y: i32,
}
```

Here, we have used the `derive` attribute to automatically generate an implementation of the `Debug` trait for our `Point` struct. This will create a `debug` method that returns a formatter that prints the `x` and `y` fields of the struct.

With this implementation, we can use the `println!` macro to print a `Point` value like this:

```rust
let p = Point { x: 10, y: 20 };
println!("Point: {:?}", p);
```

This will output:

```text
Point: Point { x: 10, y: 20 }
```

In summary, the `Debug` trait in Rust is a built-in trait that allows developers to print and debug Rust types. It provides a basic representation of a type suitable for debugging purposes and can be implemented for custom types by defining a debug method that returns a formatter.