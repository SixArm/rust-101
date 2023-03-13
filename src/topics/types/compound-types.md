# Compound types

In Rust, a compound type is a type that is composed of other types. There are two main compound types in Rust: tuples and arrays.

Tuples: A tuple is an ordered list of elements of different types. Tuples in Rust are declared using parentheses and the elements are separated by commas. For example, the following code creates a tuple containing a string and an integer:

```rust
let my_tuple = ("Hello, world!", 42);
```

We can access the individual elements of a tuple using indexing syntax:

```rust
let my_tuple = ("Hello, world!", 42);
let my_string = my_tuple.0;
let my_int = my_tuple.1;
```

Arrays: An array is a fixed-size collection of elements of the same type. Arrays in Rust are declared using square brackets and the elements are separated by commas. For example, the following code creates an array of integers with five elements:

```rust
let my_array = [1, 2, 3, 4, 5];
```

We can access the individual elements of an array using indexing syntax:

```rust
let my_array = [1, 2, 3, 4, 5];
let my_element = my_array[2]; // Access the third element
```

Arrays in Rust have a fixed size, which means that they cannot be resized at runtime. However, Rust provides a more flexible compound type called a vector, which can be resized dynamically.

Compound types are useful for grouping related data together and passing them around as a single unit. They also allow for more complex data structures and algorithms to be created. By using tuples and arrays effectively, Rust developers can write more efficient and maintainable code.
