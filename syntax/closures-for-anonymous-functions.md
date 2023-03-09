# Closures for anonymous functions

In Rust, closures are a type of anonymous function that can capture variables from their surrounding environment. This makes closures a powerful tool for writing functional-style code, as they allow you to create self-contained units of behavior that can be passed around and reused.

Here's an example of a simple closure in Rust:

```rust
let add = |a, b| a + b;
let result = add(3, 4);
println!("Result is {}", result);
```

In this example, we define a closure add that takes two arguments `a` and `b` and returns their sum. We then call the closure with arguments `3` and `4` and print the result.

Closures in Rust are defined using the `|` symbol to specify the arguments, followed by the closure body enclosed in braces `{}`. Rust's type inference system allows you to omit the types of the arguments, as long as they can be inferred from the context.

One important feature of Rust closures is that they can capture variables from their surrounding environment. This means that a closure can access variables that are defined outside of it, even after the original function that created the closure has returned. Here's an example:

```rust
fn main() {
    let x = 5;
    let add_x = |y| x + y;
    let result = add_x(3);
    println!("Result is {}", result);
}
```

In this example, we define a closure `add_x` that takes an argument `y` and adds it to the variable `x` that is already defined outside of the closure. When we call the closure with argument `3`, it captures the value of `x` and returns `8`.

Rust closures can also be used to create iterators, which are a powerful tool for working with collections of data. For example, the map method on a Vec can be used to apply a closure to each element of the vector:

```rust
let numbers = vec![1, 2, 3, 4];
let squares = numbers.iter().map(|x| x * x);
for square in squares {
    println!("Square is {}", square);
}
```

In this example, we define a vector of numbers, then use the `iter` method to create an iterator over the vector's elements. We then use the `map` method to apply a closure that squares each element of the vector. Finally, we loop over the resulting iterator and print each square.

Overall, Rust closures are a powerful feature that can be used for a wide variety of tasks, from simple arithmetic to complex functional programming.
