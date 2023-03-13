# Display trait for formatting

In Rust, the `Display` trait is a built-in trait that allows developers to format a value as a string for display purposes. It provides a human-readable representation of a type.

When a type implements the `Display` trait, it can be formatted as a string using the `format!` macro or the `println!` macro with the `{}` format specifier. This will use the `Display` implementation to convert the value into a string that can be displayed.

To implement the `Display` trait for a custom type, we define a `fmt` method on the type that takes a formatter object. The formatter object implements the `fmt::Write` trait, which provides methods for writing to a string buffer.

For example, let's consider a simple Point struct:

```rust
use std::fmt;

struct Point {
    x: i32,
    y: i32,
}

impl fmt::Display for Point {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "({}, {})", self.x, self.y)
    }
}
```

Here, we define a `fmt` method for the `Display` trait on our `Point` struct. This method takes a formatter object and formats the `x` field and `y` field of the struct into a string that is suitable for display. We use the `write!` macro to write the fields into the formatter object.

With this implementation, we can use the `format!` macro to format a Point value as a string like this:

```rust
let p = Point { x: 10, y: 20 };
let s = format!("Point: {}", p); // The result is "Point: (10, 20)"
```

In summary, the `Display` trait in Rust is a built-in trait that allows developers to format a value as a string for display purposes.