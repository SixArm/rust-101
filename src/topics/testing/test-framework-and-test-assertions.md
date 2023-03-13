# Test framework and test assertions

Rust has a built-in testing framework that allows developers to write and run automated tests for their Rust code. The testing framework is designed to be easy to use, and it supports a wide range of testing scenarios, including unit tests, integration tests, and benchmark tests.

To write tests in Rust, developers create test functions that are annotated with the #[test] attribute. These functions can contain one or more test assertions that check whether a particular condition is true or false. If all assertions in a test function pass, the test is considered to have passed. If any assertion fails, the test is considered to have failed.

Here's an example of a simple test function in Rust:

```rust
#[test]
fn test_addition() {
    let result = 2 + 2;
    assert_eq!(result, 4);
}
```

In this example, the `test_addition` function tests whether the addition of two numbers results in the expected value. The `assert_eq!` macro compares the result of the addition with the expected value of 4. If the addition results in anything other than 4, the assertion will fail, and the test will fail.

To run tests in Rust, developers use the `cargo test` command, which runs all tests in a Rust project and reports the results. The cargo test command can also be used to run specific tests or groups of tests, and it provides a range of options for controlling the behavior of the testing framework.

In addition to unit tests, Rust's testing framework also supports integration tests, which test the interaction between different modules or components of a Rust application, and benchmark tests, which measure the performance of Rust code under different conditions.

Overall, Rust's built-in testing framework provides a convenient and efficient way to write and run automated tests for Rust code, making it easy to ensure that Rust applications are correct, reliable, and performant.


## Test assertions

The Rust testing framework provides macros for writing test assertions, including:

* `assert_eq!(a, b)` and `assert_ne!(a, b)`: Checks whether two values are equal or not equal, respectively.

* `assert!(condition)`: Checks whether a condition is true.

* `assert!(condition, message)`: Checks whether a condition is true, and includes a custom error message if the condition is false.

* `assert!(condition, message, value)`: Checks whether a condition is true, and includes a custom error message that includes the value of a variable if the condition is false.

The Rust Assertables crate provides more macros for writing more kinds of test assertions, including:

* `assert_gt!(a, b)` and `assert_lt!(a, b)`: Checks whether the first value is greater than the second value, or less than it, respectively.

* `assert_starts_with!(string, substring)`: Checks whether the string starts with the substring.

* `assert_contains(array, element)`: Checks whether the array contains the element.

* `assert_is_match(regex, string)`: Checks whether the regular expression regex matches the string.

* `assert_fn_eq!(function1, function2)`: Checks whether two funcions return equal results.
