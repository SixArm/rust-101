# enum keyword for enumerations

In Rust, an enum (short for "enumeration") is a custom data type that allows you to define a set of named values. Each value is called a variant, and you can use an enum to represent a fixed set of possible values for a particular data type.

Here's an example of an enum in Rust:

```rust
enum Color {
    Red,
    Green,
    Blue,
}
```

In this example, we've defined an enum called `Color` with three variants: `Red`, `Green`, and `Blue`. We can use this enum to represent a color value in our Rust program.

Enums in Rust can also include data associated with each variant. Here's an example:

```rust
enum IPAddress {
    V4(u8, u8, u8, u8),
    V6(String),
}
```

In this example, we've defined an enum called `IPAddress` with two variants: `V4` and `V6`. The `V4` variant includes four `u8` values representing the four octets of an IPv4 address, while the V6 variant includes a single `String` value representing an IPv6 address.

Enums in Rust can be useful for a variety of programming tasks, including defining states for a state machine, representing different types of errors, and creating custom data types for your program. Rust's enums are type-safe and flexible, making them a powerful tool for Rust programmers.
