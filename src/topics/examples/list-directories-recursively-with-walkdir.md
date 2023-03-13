# List directories recursively with walkdr

Rust example code to list directories recursively with the walkdr crate.

```rust
use walkdir::{DirEntry, WalkDir};

fn list_directories_recursively(start_path: &str) {
    for entry in WalkDir::new(start_path) {
        let path = entry.unwrap().path();
        println!("{}", path.display());
        if path.is_dir() {
            list_directories(&path.to_string_lossy());
        }
    }
}

fn main() {
    list_directories("/path/to/start_directory");
}
```

This example does these steps:

1. Import the "walkdir" crate in your Rust project.

2. Define the starting directory and create a WalkDir object.

3. Use a for loop to iterate over each entry in the WalkDir object.

6. Print the file path.

4. Check if the current entry is a file or directory.

5. If it is a directory, recursively call the function on that directory.
