# Memory ownership and borrowing

Rust uses a unique system for managing memory called "ownership". Ownership is a key concept in Rust, which helps ensure memory safety and prevents many common programming errors such as null pointer dereferencing, use-after-free, and data races.

In Rust, each value has an owner, which is responsible for managing the memory associated with that value. When a value is created, its ownership is assigned to the variable that holds it. Ownership can then be transferred to another variable, passed as a function argument, or returned from a function. When the variable that owns a value goes out of scope, the value is automatically deallocated.

This ownership model allows Rust to guarantee memory safety at compile-time, without the need for a garbage collector or manual memory management. It does so by enforcing a set of rules that ensure that each value is owned by only one variable at a time, that ownership can be transferred but not shared, and that every value is deallocated exactly once when it goes out of scope.

In addition to ownership, Rust also provides a mechanism for borrowing, which allows multiple variables to have temporary access to a value without taking ownership of it. This allows for efficient and flexible memory management, while still ensuring that memory safety is maintained.

Overall, Rust's memory ownership model provides a powerful and safe way to manage memory in a concurrent and parallel programming environment.

TODO: example
