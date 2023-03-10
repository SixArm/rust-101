# Send and Sync traits for multithreading

Rust provides two important traits that are related to concurrency and multithreading: `Send` and `Sync`.

The `Send` trait in Rust indicates that a type is safe to be sent across thread boundaries. This means that if a type implements the `Send` trait, it can be safely passed from one thread to another without causing any data races or undefined behavior. For example, the `String` type in Rust implements the `Send` trait, which means it can be safely shared across multiple threads.

To implement the `Send` trait for a custom type, all of its fields must also implement the `Send` trait. This is because if a type contains non-`Send` fields, it may be possible for data races to occur when the type is shared across threads. The `Send` trait is automatically implemented for most primitive types in Rust, as well as many standard library types like `Vec` and `String`.

To summarize, the Send trait ensures that a type can be safely transferred between threads, while the Sync trait ensures that a type can be safely shared between threads. These traits are important for writing safe and efficient concurrent Rust code.


## Send trait details

Here's an example of a custom type that implements the `Send` trait:

```rust
struct Foo {
    x: i32,
    y: String,
}

unsafe impl Send for Foo {}

fn main() {
    let foo = Foo { x: 42, y: "Hello, world!".to_string() };
    std::thread::spawn(move || {
        println!("x = {}, y = {}", foo.x, foo.y);
    });
}
```

In this example, the `Foo` struct contains an `i32` field and a `String` field. Since both `i32` and `String` implement the `Send` trait, we can manually implement `Send` for `Foo` using the `unsafe impl Send for Foo {}` syntax. We can then safely pass a `Foo` instance to a new thread using `std::thread::spawn`, and access its fields from within the thread without causing any data races.


## Sync trait details

The `Sync` trait in Rust indicates that a type is safe to be shared between multiple threads. This means that if a type implements the `Sync` trait, it can be safely accessed from multiple threads without causing any data races or undefined behavior. For example, the `Arc` type in Rust implements the `Sync` trait, which means it can be safely shared between multiple threads.

Here's an example of how the Sync trait can be used:

```rust
use std::sync::Arc;

struct MyStruct {
    // ...
}

impl MyStruct {
    fn do_something(&self) {
        // ...
    }
}

// Create a shared instance of MyStruct that can be safely accessed from multiple threads
let shared = Arc::new(MyStruct { /* ... */ });

// Spawn a new thread that will use the shared instance
std::thread::spawn({
    let shared = shared.clone();
    move || {
        shared.do_something();
    }
});
```

In this example, we create a shared instance of `MyStruct` using the `Arc` type, which automatically implements the `Sync` trait. We can then safely access the shared instance from multiple threads, without worrying about synchronization issues.

The `Sync` trait is automatically implemented for any type that satisfies the following conditions: the type is `Send`, which means that it can be safely moved between threads, and the type does not have any interior mutability, which means that there are no mutable references to the type's contents.
