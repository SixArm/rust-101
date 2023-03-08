# Unsafe code

Rust is a programming language that prioritizes safety and correctness. However, there are situations where you may need to bypass Rust's built-in safety checks to perform certain operations. In these cases, Rust provides a way to write unsafe code within a safe Rust program.

Unsafe code is Rust code that the compiler cannot verify for safety at compile-time. This code is typically used when working with low-level operations that require direct access to system resources or when interacting with code written in other programming languages.

In unsafe code, Rust allows the use of several features that are not permitted in safe code, including:

* Dereferencing raw pointers: Raw pointers are unmanaged pointers that do not have any safety guarantees. Dereferencing raw pointers can lead to undefined behavior, such as null pointer dereferences, use-after-free errors, and other memory-related bugs.

* Calling unsafe functions: Unsafe functions are Rust functions that are marked with the unsafe keyword. These functions can perform operations that are not safe to perform in safe Rust code, such as accessing memory directly or performing system-level operations.

* Modifying global state: Rust's ownership and borrowing system ensures that data is accessed safely and not modified concurrently. However, in unsafe code, you can bypass these guarantees and modify global state directly, which can lead to race conditions and other issues.

It's important to note that just because code is marked as unsafe doesn't mean it's inherently dangerous or incorrect. Unsafe code is often necessary for performance-critical code, interfacing with external systems, or implementing low-level abstractions.

However, writing and working with unsafe code requires a deep understanding of Rust's memory and ownership model, as well as a strong understanding of the system being interfaced with. Rust also provides several tools, such as unsafe blocks, to help ensure that unsafe code is written and used correctly.
