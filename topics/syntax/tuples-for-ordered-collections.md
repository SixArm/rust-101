# Tuples for ordered collections

In Rust, a tuple is an ordered collection of values with a fixed length. Tuples can contain values of different types and are represented using parentheses with the values separated by commas.

Here is an example of a tuple containing two values, a string and an integer:

```rust
let person = ("Alice", 30);
```

This defines a tuple called `person` containing the string `"Alice"` and the integer `30`. Tuples can be assigned to variables, passed as function arguments, and returned as function results, just like any other value in Rust.

You can access individual elements of a tuple using dot notation and the index of the element you want to access, starting from zero. For example:

```rust
let name = person.0;
let age = person.1;
```

This assigns the first element of the person tuple, which is the string `"Alice"`, to the `name` variable, and the second element, which is the integer `30`, to the `age` variable.

Tuples are often used to return multiple values from a function. For example, the `std::fs::metadata` function returns a `Result<std::fs::Metadata>` object, which contains information about a file or directory, such as its size and permissions. The `std::fs::metadata` function returns a tuple containing the `std::fs::Metadata` object and the `std::io::Result` object, which contains information about any errors that occurred:

```rust
use std::fs;

fn main() -> std::io::Result<()> {
    let metadata = fs::metadata("file.txt")?;
    let (size, permissions) = (metadata.len(), metadata.permissions());
    println!("File size: {} bytes", size);
    println!("Permissions: {:?}", permissions);
    Ok(())
}
```

This calls the `std::fs::metadata` function to retrieve the metadata for the file `file.txt`. It then extracts the file size and permissions from the `std::fs::metadata` object using a tuple and prints them to the console.

In summary, a tuple in Rust is an ordered collection of values with a fixed length. Tuples can contain values of different types and are represented using parentheses () with the values separated by commas.
