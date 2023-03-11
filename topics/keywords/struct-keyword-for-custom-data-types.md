# struct keyword for custom data types

In Rust, a struct is a custom data type that allows you to group together related data items and functions that operate on that data. A struct can be defined using the `struct` keyword, followed by the name of the struct and a block of curly braces that contains the fields of the struct.

Here is an example of a struct definition in Rust:

```rust
struct Rectangle {
    width: u32,
    height: u32,
}
```

In this example, we define a struct named `Rectangle` that has two fields: `width` and `height`, both unsigned 32-bit integer types.

Structs can also have functions associated with them, called methods. Methods are defined within the block of curly braces after the fields of the struct, and can be used to operate on the data within the struct. For example:

```rust
impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }
}
```

This example uses `impl` to define an implementation block for the `Rectangle` struct, and defines a method named `area` that calculates the area of the rectangle. The `&self` parameter indicates that the method takes a reference to the struct as its first argument.

Once a struct is defined, you can create instances of the struct by calling its constructor function, which is the name of the struct followed by `::new`. For example:

```rust
let r = Rectangle { width: 10, height: 20 };
```

This creates a new `Rectangle` struct with a `width` field of 10, and an `height` field of 20.

Overall, structs in Rust provide ways to define custom data types with associated functions and methods, making it easy to organize and manipulate complex data structures.