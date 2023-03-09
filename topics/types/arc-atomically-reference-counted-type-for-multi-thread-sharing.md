# Arc (Atomically Reference Counted) for multi-thread sharing

In Rust, `Arc` (Atomically Reference Counted) is a smart pointer that provides shared ownership of a value, similar to `Rc` (Reference Counted) smart pointer. The difference is that `Arc` can be safely shared between threads, making it useful for concurrent programming.

`Arc` works by keeping track of the number of references to a value, and ensuring that the value is not dropped until all references have been dropped. When a new reference to the value is created, `Arc` increments the reference count, and when a reference is dropped, `Arc` decrements the reference count. When the reference count reaches zero, `Arc` drops the value.

`Arc` provides a way to share ownership of a value between multiple threads, allowing multiple threads to access the value concurrently. When an `Arc` is cloned, a new pointer to the same value is created, and the reference count is incremented. Because `Arc` uses atomic operations to increment and decrement the reference count, it can be safely shared between threads.

For example, consider the following code:

```rust
use std::sync::Arc;
use std::thread;

fn main() {
    let shared_data = Arc::new(vec![1, 2, 3]);

    for i in 0..3 {
        let data = shared_data.clone();

        thread::spawn(move || {
            let result = data.iter().map(|x| x + i).collect::<Vec<_>>();
            println!("{:?}", result);
        });
    }
}
```

Here, an `Arc` is used to share ownership of a vector between multiple threads. The `Arc::new()` function is used to create a new `Arc` that points to a vector of [1, 2, 3]. The `clone()` method is used to create a new `Arc` that points to the same vector, and the reference count is incremented. The `thread::spawn()` function is used to create three threads, each of which iterates over the vector and adds the current loop index to each element. The results are collected into a new vector, which is printed to the console.

`Arc` is a useful tool for concurrent programming in Rust, allowing multiple threads to safely share ownership of a value. By using atomic operations to manage the reference count, `Arc` ensures that the value is not dropped until all references to it have been dropped.
