# Match keyword and match arms for control flow

In Rust, the `match` keyword is a powerful control flow construct that allows a program to match a value against a set of patterns and execute code based on the match result. The `match` keyword and statement is similar to a `switch` keyword and statement in other languages, but `match` provides more powerful pattern matching capabilities.

A match statement typically has the following syntax:

```rust
match <value> {
    <pattern_1> => <code_1>,
    <pattern_2> => <code_2>,
    ...
    <pattern_n> => <code_n>,
}
```

The `<value>` is the expression that is being matched against, and the `<pattern>` expressions are the patterns that are being matched. Each `<pattern>` is followed by a `=>` symbol, then a block of code that will be executed if the pattern matches the value.

In Rust, a pattern can take many forms, including:

* Literal values: e.g. `42`, `"hello"`

* Variables: e.g. `x`, `y`

* Wildcards: e.g. `_`

* Ranges: e.g. `1..=5`

* Enums: e.g. `Some(value)`

* Structs: e.g. `Point { x, y }`

* Tuples: e.g. `(x, y)`

The code in each match arm is executed if the pattern on the left-hand side of the `=>` operator matches the value being matched. If none of the patterns match, the `match` statement will panic at runtime.

Rust's `match` statements are powerful and flexible, allowing for complex patterns and expressions to be matched. Match statements are commonly used in Rust to handle errors, parse command-line arguments, and implement state machines, among other use cases.

Overall, match statements are a key feature of Rust's control flow syntax, and provide a powerful mechanism for pattern matching and value extraction in Rust programs.
