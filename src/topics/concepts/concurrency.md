# Concurrency

Rust concurrency is based on the ownership and borrowing model, which guarantees memory safety and eliminates data races.

Rust has several concurrency primitives, such as threads, channels, mutexes, and atomic operations. Rust's threading model is based on the fork-join model, where a program creates multiple threads to perform different tasks, and the threads join back together at the end.

Here is an example code snippet that demonstrates Rust concurrency using threads:

```rust
use std::thread;

fn main() {
    let mut handles = vec![];
    for i in 0..5 {
        // Create a new thread
        let handle = thread::spawn(move || {
            println!("Hello from thread {}", i);
        });
        // Store the thread handle
        handles.push(handle);
    }
    // Wait for all threads to finish
    for handle in handles {
        handle.join().unwrap();
    }
}
```

In this example, the `thread::spawn()` function creates a new thread, and the `move` keyword moves the variable `i` into the closure. The closure prints a message indicating which thread it is running on.

The `handles` vector stores the handles of all the threads that were created. Finally, the `join()` method is called on each thread handle to wait for the thread to finish before exiting the program.

This is just a basic example, but Rust's concurrency primitives can be combined in various ways to build more complex and efficient concurrent programs.
