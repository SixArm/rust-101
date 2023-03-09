# Copy trait and Clone trait for duplication

In Rust, the Copy trait is used to control how values are copied, while the Clone trait is used to control how values are cloned.

The `Copy` trait is used for types that can be safely copied bit-by-bit, without any special consideration for ownership or memory management. When a value with the `Copy` trait is assigned to a new variable or passed to a function, a bitwise copy of the original value is made. This means that the original value remains unchanged, and any changes made to the copied value do not affect the original.

Examples of types that implement the `Copy` trait include simple scalar types like integers and booleans, as well as tuples and arrays that only contain types that implement the `Copy` trait.

The `Clone trait`, on the other hand, is used for types that need to be explicitly cloned in order to make a copy. When a value with the `Clone` trait is cloned, a new instance of the value is created, and any owned data is also cloned. This means that changes made to the cloned value do not affect the original, and vice versa.

To implement the `Clone` trait for a type, you need to provide an implementation of the `clone` method, which creates a new instance of the type and clones any owned data. Rust also provides a default implementation of `Clone` for types that implement the `Copy` trait, which simply returns a bitwise copy of the value.

In summary, the `Copy` trait is used for types that can be copied bit-by-bit, while the `Clone` trait is used for types that need to be explicitly cloned in order to make a copy.
