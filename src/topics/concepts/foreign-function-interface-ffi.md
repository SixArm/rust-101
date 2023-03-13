# Foreign Function Interface (FFI)

In Rust, the Foreign Function Interface (FFI) allows Rust code to interoperate with code written in other languages, such as C or C++. This enables Rust to be used in mixed-language projects or to use existing libraries that are written in other languages.

To use the FFI in Rust, you first need to declare an external function or type from another language using the `extern` keyword:

```rust
extern "C" {
    fn some_function(arg1: i32, arg2: *mut i32) -> i32;
}
```

This declares a function called `some_function` that takes an `i32` and a pointer to an `i32` as arguments and returns an `i32`. The "C" string in the `extern` declaration specifies the calling convention, which tells the Rust compiler how to interact with the external function.

To call this function from Rust, you can use the `unsafe` keyword to tell the Rust compiler that the function call is unsafe and may have side effects:

```rust
let arg1 = 42;
let mut arg2 = 0;
let result = unsafe { some_function(arg1, &mut arg2) };
```

This calls the `some_function` function with the specified arguments, passing a mutable reference to `arg2` using the `&mut` operator.

Rust also provides a `#[no_mangle]` attribute that can be used to disable Rust's name mangling, which can be useful when interacting with external libraries. For example, you can declare a Rust function with the `#[no_mangle]` attribute and call it from C code.

In summary, the Rust FFI enables Rust code to interoperate with code written in other languages, and can be used to call external functions from Rust or to expose Rust functions to other languages.
