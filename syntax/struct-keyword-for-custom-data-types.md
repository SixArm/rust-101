# struct keyword for custom data types

In Rust, a struct is a custom data type that allows you to group together related data items and functions that operate on that data. A struct can be defined using the `struct` keyword, followed by the name of the struct and a block of curly braces that contains the fields of the struct.

Here is an example of a struct definition in Rust:

```rust
struct Person {
    name: String,
    age: u32,
}
```

In this example, we define a struct named `Person` that has two fields: `name` and `age`. The `name` field is a `String` type, and the `age` field is an unsigned 32-bit integer.

Structs can also have functions associated with them, called methods. Methods are defined within the block of curly braces after the fields of the struct, and can be used to operate on the data within the struct.

Here is an example of a struct with a method in Rust:

```rust
struct Rectangle {
    width: u32,
    height: u32,
}

impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }
}
```

In this example, we define a struct named `Rectangle` that has two fields: `width` and `height`. We then define an implementation block for the `Rectangle` struct using the `impl` keyword, and define a method named `area` that calculates the area of the rectangle. The `&self` parameter indicates that the method takes a reference to the struct as its first argument.

Once a struct is defined, you can create instances of the struct by calling its constructor function, which is the name of the struct followed by `::new`. For example, to create a new `Person` struct, you can do the following:

```rust
let person = Person { name: String::from("John Doe"), age: 30 };
```

This creates a new `Person` struct with a `name` field of "John Doe" and an `age` field of 30.

Overall, structs in Rust provide a powerful and flexible way to define custom data types with associated functions and methods, making it easy to organize and manipulate complex data structures.