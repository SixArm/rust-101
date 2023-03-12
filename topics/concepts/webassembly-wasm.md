# WebAssembly (WASM)

WebAssembly (WASM) is a binary instruction format that allows code to be executed in a sandboxed environment on web browsers, outside of the JavaScript runtime. Rust is one of the programming languages that can be compiled to WebAssembly, which allows Rust code to be executed in web browsers and other WASM environments.

Rust's support for WebAssembly comes through the Rust stdweb and wasm-bindgen crates, which provide tools for interacting with the WASM environment from Rust code. These crates allow Rust code to be compiled to WASM and provide a bridge between Rust and JavaScript, enabling Rust functions to be called from JavaScript and vice versa.

One of the main benefits of using Rust for WebAssembly is performance. Rust's focus on low-level control and efficient memory management make it a good fit for WASM, which has similar performance requirements to native code. Additionally, Rust's ownership and borrowing model can help prevent memory-related bugs in WASM code, which is especially important in the security-sensitive environment of the web.

Rust's support for WebAssembly also extends beyond the web. WASM can be run in a variety of environments, including mobile devices, IoT devices, and server-side applications. Rust's cross-platform support and memory safety features make it a good choice for developing WASM applications that can run on a variety of platforms.

Overall, Rust's support for WebAssembly makes it a powerful tool for developing high-performance, secure, and cross-platform applications that can be executed in a variety of environments, including web browsers.


## Example

Here is a simple Rust programming example for WebAssembly (WASM):

1. First, you need to install Rust and the necessary tools for building WebAssembly applications. You can follow the instructions here: https://www.rust-lang.org/tools/install

2. Create a new Rust project by running the following command in your terminal:

```
cargo new wasm-example --lib
```

This command will create a new Rust project called `wasm-example` with a `lib.rs` file in the `src/` directory.

3. Add the `wasm-bindgen` dependency to your `Cargo.toml` file. This library provides Rust bindings for JavaScript and makes it easy to call Rust functions from JavaScript:

```
[dependencies]
wasm-bindgen = "0.2.72"
```

4. In your `lib.rs` file, add the `wasm_bindgen` macro to the top of the file:

```rust
use wasm_bindgen::prelude::*;
```

5. Define a simple Rust function that takes two numbers and returns their sum:

```rust
#[wasm_bindgen]
pub fn add(a: i32, b: i32) -> i32 {
    a + b
}
```

6. Build your Rust code as a WebAssembly module by running the following command:

```
cargo +nightly build --target wasm32-unknown-unknown --release
```

This will create a WASM file called `wasm-example.wasm` in the `target/wasm32-unknown-unknown/release/` directory.

7. Finally, create a JavaScript file that loads the WASM module and calls your Rust function:

```javascript
import("./wasm_example_bg.wasm").then((module) => {
  const { add } = module;

  console.log(add(1, 2)); // outputs 3
});
```

This JavaScript code loads the WASM module using the `import()` function, which is a new feature in JavaScript that allows you to dynamically load modules at runtime. Once the module is loaded, you can call your Rust function using the `add` variable.
