# Assertables crate for assert macro tests

Link: <https://crates.io/crates/assertables>

The Rust Assertables crate is a library for assert macro functionality, for Rust testing, validation, and verification.

To use Tokio, you first need to add it to your project's dependencies in your `Cargo.toml` file:

```toml
[dependencies]
assertables = "7"
```

Here's a simple example of how to use the Assertables crate to test that one value is less than another value:

```rust
#[cfg(test)]
mod test_assert_x_result {
    use assertables;

    #[test]
    fn test_example() {
        let x = 1;
        let y = 2;
        assert_lt!(x, y);
    }
```

In this example, we define a test function `test_example`. We use the Assertables `assert_lt!` macro to test that `x` is less than `y`. If the assert macro succeeds, then the test completes normally. If the assert macro fails, then the macro prints an error message with specific debugging information.

Here's an example of how to use the Assertables crate to test strings:

```rust
#[cfg(test)]
mod test_assert_x_result {
    use assertables;

    #[test]
    fn test_example() {
        let string1 = "Hello World";
        let string2 = "He";
        assert_starts_with!(string1, string2); 
    }
```

The Assertable crate provides a range of macros for compile-time testing, as well as debug macros for non-optimized runtime debugging, and runtime macros for optimized runtime validation and verification.

Overall, the Assertables crate provides more power and flexibility to do test assertions, making it easier to build clear reliable tests for your Rust programs.
