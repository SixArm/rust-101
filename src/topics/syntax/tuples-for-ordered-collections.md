# Tuples for ordered collections

In Rust, a tuple is an ordered collection of values with a fixed length. Tuples can contain values of different types and are represented using parentheses with the values separated by commas.

Here is an example of a tuple containing two values, a string and an integer:

```rust
let person = ("Alice", 30);
```

This defines a tuple called `person` containing the string "Alice" and the integer `30`. Tuples can be assigned to variables, passed as function arguments, and returned as function results, just like any other value in Rust.

You can access individual elements of a tuple using dot notation and the index of the element you want to access, starting from zero. For example:

```rust
let name = person.0;
let age = person.1;
```

Tuples are often used to return multiple values from a function. For example, the `std::fs::metadata` function returns a result that is tuple, and contains information about a file or directory, such as its size and permissions:

```rust
use std::fs;

fn main() -> std::io::Result<()> {
    let metadata = fs::metadata("file.txt")?; // get metadata for the file
    let (size, permissions) = (metadata.len(), metadata.permissions()); // extract to a tuple
    println!("File size is {} bytes, and permisisons are {}", size, permissions);
    Ok(())
}
```

In summary, a tuple in Rust is an ordered collection of values with a fixed length. Tuples can contain values of different types and are represented using parentheses () with the values separated by commas.
