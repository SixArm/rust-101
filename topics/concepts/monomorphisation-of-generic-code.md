# Monomorphisation

Rust monomorphization is a process where generic code is transformed into specific code for each concrete type used in the program. In other words, it is the process of generating specialized code for each type that is used in a generic function or struct.

This is different from traditional dynamic dispatch, where a function or method call is resolved at runtime, based on the type of the object or value being operated on. With monomorphization, the specific implementation of a generic function is determined at compile-time, and there is no runtime overhead associated with dynamic dispatch.

Monomorphization in Rust is enabled by the language's support for generics, which allows code to be written once and used with multiple different types. When generic code is compiled, Rust creates specialized copies of the code for each type it is used with, effectively turning the generic code into a collection of concrete, monomorphic functions. This makes Rust code faster and more efficient than code that relies on dynamic dispatch, as there is no need for the program to perform costly runtime lookups to determine which implementation to use.

Overall, Rust's monomorphization allows developers to write generic code that is as fast as hand-written, specific code, without having to duplicate code for each type they want to use it with. This makes Rust a powerful and efficient language for building large-scale applications.

TODO: example
