# Range syntax for a sequence of values

In Rust, a range is a way to represent a sequence of values between a start and end point. A range are defined using the syntax `start..end`, where `start` is the first value in the range, and `end` is the first value not in the range.

Here are some examples of Rust ranges:

```rust
let a = 0..10;  // range from 0 to 9 inclusive
let b = 1..=10; // range from 1 to 10 inclusive
let c = ..5;    // range from the start up to (but not including) 5
let d = 5..;    // range from 5 to infinity
```

Ranges can be used in many contexts in Rust, such as in for loops:

```rust
for i in 0..10 {
    println!("{}", i);
}
```

This will print the numbers from 0 to 9.

Ranges can also be used with various methods provided by the `Iterator` trait, such as `map`, `filter`, `fold`, and more:

```rust
let nums = (0..10).filter(|x| x % 2 == 0).map(|x| x * 2).collect::<Vec<_>>();
// nums is now [0, 4, 8, 12, 16]
```

This creates a range from 0 to 9, filters out any odd numbers, doubles the remaining even numbers, and collects them into a vector.

Overall, Rust ranges are a flexible and convenient way to represent sequences of values, and they are widely used throughout the language.
