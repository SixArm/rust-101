# Memory on the stack or the heap

In Rust, memory is typically allocated either on the stack or the heap. The stack and heap are two different regions of memory that are used for different purposes.

The stack is a region of memory that is used for storing local variables and function call frames. Each time a function is called, a new stack frame is created to store the function's local variables and other data. When the function returns, its stack frame is destroyed, and the memory used by the stack frame is released.

Stack allocation is fast and efficient, because the memory for a stack frame is allocated when the function is called, and released when the function returns. This means that stack allocation doesn't require any runtime overhead, making it an excellent choice for small, short-lived objects.

On the other hand, the heap is a region of memory that is used for dynamically allocated data. Data allocated on the heap persists until it is explicitly deallocated. Heap allocation can be slower and less efficient than stack allocation, because it requires additional runtime overhead to allocate and deallocate memory.

In Rust, heap allocation is typically done using the Box type, which creates a pointer to a value that is stored on the heap. For example:

```rust
fn main() {
    let x = Box::new(5);
    println!("{}", x);
}
```

Here, `x` is a pointer to a value of 5 that is stored on the heap. The `Box::new()` function allocates memory on the heap and returns a pointer to the allocated memory. The `println!()` macro prints the value of `x`.

Rust's ownership and borrowing system helps ensure that heap-allocated memory is used safely and efficiently. By enforcing strict rules around memory management, Rust makes it possible to write high-performance, memory-safe code without the need for garbage collection or other runtime memory management.
