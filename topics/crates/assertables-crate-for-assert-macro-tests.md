# Assertables crate for assert macro tests

<https://crates.io/crates/assertables>

The Rust Assertables crate is a library for assert macro functionality, for Rust testing, validation, and verification. If an assert macro succeeds, then it completes normally. If an assert macro fails, then it prints an error message with debugging information. 

To use Asseretables, add it to your project's dependencies in your `Cargo.toml` file:

```toml
[dependencies]
assertables = "7"
```

Here's a simple example of how to use the Assertables crate:

```rust
#[cfg(test)]
mod test_assert_x_result {
    use assertables;

    #[test]
    fn example1() {
        let x = 1;
        let y = 2;
        assert_lt!(x, y);
    }

    #[test]
    fn example2() {
        let string1 = "Hello World";
        let string2 = "He";
        assert_starts_with!(string1, string2); 
    }
}
```

In the `example1` function, we use the `assert_lt!` macro to test that `x` is less than `y`. In the `example2` function, we use the `assert_starts_with!` macro to test that `string1` starts with `string2`.

The Assertable crate provides a range of macros for compile-time testing, as well as debug macros for non-optimized runtime debugging, and runtime macros for optimized runtime validation and verification.

Overall, the Assertables crate provides more power and flexibility to do test assertions, making it easier to build clear reliable tests for your Rust programs.
