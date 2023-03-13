# WebAssembly (WASM)

WebAssembly (WASM) is a binary instruction format that allows code to be executed in a sandboxed environment on web browsers, outside of the JavaScript runtime. Rust is one of the programming languages that can be compiled to WebAssembly, which allows Rust code to be executed in web browsers and other WASM environments.

Rust's support for WebAssembly comes through the Rust stdweb and wasm-bindgen crates, which provide tools for interacting with the WASM environment from Rust code. These crates allow Rust code to be compiled to WASM and provide a bridge between Rust and JavaScript, enabling Rust functions to be called from JavaScript and vice versa.

One of the main benefits of using Rust for WebAssembly is performance. Rust's focus on low-level control and efficient memory management make it a good fit for WASM, which has similar performance requirements to native code. Additionally, Rust's ownership and borrowing model can help prevent memory-related bugs in WASM code, which is especially important in the security-sensitive environment of the web.

Rust's support for WebAssembly also extends beyond the web. WASM can be run in a variety of environments, including mobile devices, IoT devices, and server-side applications. Rust's cross-platform support and memory safety features make it a good choice for developing WASM applications that can run on a variety of platforms.

To use the WASM crate, add the dependency to your project `Cargo.toml` file:

```
[dependencies]
wasm-bindgen = "0.2.72"
```

Overall, Rust's support for WebAssembly makes it a powerful tool for developing high-performance, secure, and cross-platform applications that can be executed in a variety of environments, including web browsers.

<div style="page-break-before:always">&nbsp;</div><p></p>

## WebAssembly (WASM) example

Create a new Rust project, such as running `cargo new wasm-example --lib`, and add the `wasm-bindgen` dependency to your `Cargo.toml` file. 

In your `lib.rs` file, add the `wasm_bindgen` macro to the top of the file, and define a simple Rust function that takes two numbers and returns their sum:

```rust
use wasm_bindgen::prelude::*;

#[wasm_bindgen]
pub fn add(a: i32, b: i32) -> i32 {
    a + b
}
```

Build your Rust code as a WebAssembly module by running the following command, which creates a WASM file called `wasm-example.wasm` in the `target/wasm32-unknown-unknown/release/` directory:


```sh
cargo +nightly build --target wasm32-unknown-unknown --release
```

Finally, create a JavaScript file that loads the WASM module and calls your Rust function:

```javascript
import("./wasm_example_bg.wasm").then((module) => {
  const { add } = module;
  console.log(add(1, 2)); // outputs 3
});
```

This JavaScript code loads the WASM module using the `import()` function, which is a new feature in JavaScript that allows you to dynamically load modules at runtime. Once the module is loaded, you can call your Rust function using the `add` variable.
