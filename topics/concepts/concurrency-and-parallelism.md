# Concurrency and parallelism

In Rust, concurrency refers to the ability of a program to perform multiple tasks or operations at the same time, while parallelism refers to the ability of a program to perform multiple tasks or operations simultaneously, using multiple processors or cores.

Rust provides several mechanisms for concurrency and parallelism, including:

* Threads: Rust's standard library provides a low-level interface for creating and managing threads. Threads allow a program to execute multiple tasks in parallel, but require careful synchronization to avoid data races and other concurrency issues.

* Channels: Rust's channels provide a high-level mechanism for communication between threads. Channels allow multiple threads to send and receive data, and ensure that the data is transmitted in a synchronized and safe manner.

* Futures: Rust's futures provide a mechanism for asynchronous programming, allowing a program to perform non-blocking I/O and other operations without blocking the main thread. Futures are composable and can be combined to create complex asynchronous workflows.

* Atomic types: Rust's atomic types provide a safe and efficient way to share data between threads. Atomic types are designed to be thread-safe, and provide operations that ensure that data is updated atomically, without the need for locks or other synchronization mechanisms.

Rust's concurrency and parallelism mechanisms are designed to be safe and efficient, and take advantage of Rust's ownership and borrowing system to prevent data races and other concurrency issues. Additionally, Rust's compiler provides powerful static analysis and optimization tools that can help identify and eliminate potential issues in concurrent and parallel code.

Overall, Rust's concurrency and parallelism mechanisms provide a powerful and flexible toolkit for building concurrent and parallel programs, while ensuring that the code remains safe and efficient.


## Concurrency details

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

In this example, the `thread::spawn()` function creates a new thread, and the `move` keyword is used to move the variable `i` into the closure. The closure prints a message indicating which thread it is running on.

The `handles` vector is used to store the handles of all the threads that were created. Finally, the `join()` method is called on each thread handle to wait for the thread to finish before exiting the program.

This is just a basic example, but Rust's concurrency primitives can be combined in various ways to build more complex and efficient concurrent programs.


## Parallelism details

Rust has built-in support for parallelism, which is the ability to execute multiple tasks simultaneously on multiple processors or cores. 

Rust's support for parallelism is especially easy to use by adding the Rust `rayon` crate, which provides a high-level API for parallel programming. The `rayon` crate allows developers to easily parallelize data processing tasks, such as iterating over large collections, by abstracting away the low-level details of thread creation and synchronization.

Here is an example code snippet that demonstrates Rust parallelism using rayon:

```rust
use rayon::prelude::*;

fn main() {
    let numbers = vec![1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    let sum = numbers.par_iter().sum::<i32>();
    println!("Sum is {}", sum);
}
```

In this example, the `par_iter()` method is used to create a parallel iterator over a vector of numbers. The `sum()` method is then called on the iterator to calculate the sum of all the numbers in the vector.

`rayon` automatically divides the work among multiple threads, using as many threads as there are processors or cores available on the system. The code is executed in parallel, with each thread processing a subset of the data.

The `par_iter()` method can be used with many other methods of the standard library, such as `map()`, `filter()`, and `reduce()`, to parallelize various data processing tasks.

Overall, Rust's support for parallelism allows developers to take advantage of modern hardware and achieve high performance in their applications without sacrificing safety and correctness.
