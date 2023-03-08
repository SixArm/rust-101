# Rust namespaces and mod keyword for modules

In Rust, namespaces are a way to organize and group related items, such as functions, types, and constants, under a common name. Namespaces are implemented using modules, which are Rust's primary mechanism for organizing code into reusable components.

Modules can be defined using the `mod` keyword, followed by the name of the module and its contents enclosed in curly braces:

```rust
mod my_module {
    fn private_function() {
        // implementation details here
    }
    pub fn public_function() {
        // implementation details here
    }
}
```

In this example, `my_module` is a module that contains two functions: `private_function`, which is not visible outside of the module, and `public_function`, which is marked as pub and can be accessed from other modules.

To use a module from another module, you can use the use keyword to bring its contents into scope:

```rust
use my_module::public_function;

fn main() {
    public_function();
}
```

In this example, we bring the `public_function` from `my_module` into the scope of main, allowing us to call it directly.

Rust also provides a hierarchical module system, where modules can be nested within other modules to create a hierarchy of namespaces:

```rust
mod outer_module {
    mod inner_module {
        fn private_function() {
            // implementation details here
        }
        pub fn public_function() {
            // implementation details here
        }
    }
    use inner_module::public_function;
    pub fn call_public_function() {
        public_function();
    }
}
```

In this example, `inner_module` is nested within `outer_module`, creating a hierarchy of namespaces. We can use the `use` keyword to bring `public_function` into scope, and then call it from `call_public_function`.

Overall, namespaces in Rust provide a powerful mechanism for organizing and structuring code, enabling developers to write more modular, reusable, and maintainable software.
