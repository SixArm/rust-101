# What is a Rust "FizzBuzz" program?

In Rust, a simple "FizzBuzz" program is:

```rust
fn main() {
    for i in 1..=100 {
        if i % 3 == 0 && i % 5 == 0 {
            println!("FizzBuzz");
        } else if i % 3 == 0 {
            println!("Fizz");
        } else if i % 5 == 0 {
            println!("Buzz");
        } else {
            println!("{}", i);
        }
    }
}
```

This program prints the numbers 1 to 100, but replaces multiples of 3 with "Fizz", multiples of 5 with "Buzz", and multiples of both 3 and 5 with "FizzBuzz". This program uses a Rust `for` loop statement, some Rust `if` control flow statements that use the `%` modulo operator and `&&` logical operator, and some `println!` macros to print lines to the console.

When you run this program, you should see lines printed to the console, starting with these lines:

```text
1
2
Fizz
4
Buzz
```

