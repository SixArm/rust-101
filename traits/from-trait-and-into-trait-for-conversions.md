# From trait and Into trait for conversions

In Rust, the `From` trait and `Into` trait are used to convert values between different types. The `From` trait allows developers to define how a type can be constructed from another type, and the `Into` trait allows developers to define how a type can be converted into another type.

The `From` trait is implemented for a type and provides a `from` method that takes an argument of a different type and returns an instance of the implementing type. This allows for easy conversion between different types, especially when converting from a type that is not owned by the implementing type. For example, consider the following code:

```rust
struct MyInt(i32);

impl From<i32> for MyInt {
    fn from(val: i32) -> Self {
        MyInt(val)
    }
}

let my_int = MyInt::from(42);
```

In this code, we define a simple `MyInt` struct and implement the `From` trait for it. We define a `from` method that takes an `i32` value and returns a `MyInt` instance. This allows us to convert from an `i32` value into a `MyInt` instance, by using the `from` method. 

The `Into` trait is the opposite of the `From` trait, and is implemented for a type and provides an into method that takes no arguments and returns an instance of a different type. This allows for easy conversion between different types, especially when converting from a type that is owned by the implementing type. For example, consider the following code:

```rust
struct MyInt(i32);

impl Into<i32> for MyInt {
    fn into(self) -> i32 {
        self.0
    }
}

let my_int = MyInt(42);
let i = my_int.into();
```

In this code, we define a `MyInt` struct and implement the `Into` trait for it. We define an `into` method that takes no arguments and returns an `i32` value. This allows us to convert a `MyInt` instance into an `i32` value, by using the `into` method. 

In summary, the `From` trait and `Into` trait are used to convert values between different types. The `From` trait provides a `from` method that takes an argument of a different type and returns an instance of the implementing type, while the `Into` trait provides an `into` method that takes no arguments and returns an instance of a different type.
