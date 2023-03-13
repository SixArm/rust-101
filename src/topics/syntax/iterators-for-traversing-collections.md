# Iterators for traversing collections

In Rust, iterators are abstractions for traversing collections of data, such as arrays, vectors, and other sequences. Iterators access the elements of a collection, and can be used with many of Rust's built-in language features, such as loops and closures.

Iterators in Rust are defined by the `Iterator` trait, which provides methods for traversing and manipulating a sequence of elements. Some common methods on iterators include:

* `next()`: Returns the next iterator element, or None if there are no more.

* `map()`: Transforms each element of the iterator by applying a closure to it.

* `filter()`: Returns a new iterator that includes only the elements that match a given predicate.

* `fold()`: Reduces the iterator elements into a single value, by repeatedly applying a given function.

Here's an example of using an iterator to traverse a vector and sum up its elements:

```rust
let v = vec![1, 2, 3, 4, 5];
let sum = v.iter().fold(0, |acc, x| acc + x);
println!("The sum is: {}", sum);
```

In this example, we create a vector `v` and use the `iter()` method to create an iterator over its elements. We then use the `fold()` method to iterate over the elements, and accumule the sum of all the elements in the vector.

Iterators can also be used in loops, as in the following example:

```rust
let v = vec![1, 2, 3, 4, 5];
for i in v.iter().map(|x| x * 2) {
    println!("{}", i);
}
```

In this example, we create an iterator over the elements of the vector, and use the `map()` method to transform each element by doubling it. We then use a `for` loop to iterate over the transformed elements, and print them out one by one.

Overall, iterators are a powerful and flexible abstraction for working with collections of data in Rust, and are widely used throughout the language.
