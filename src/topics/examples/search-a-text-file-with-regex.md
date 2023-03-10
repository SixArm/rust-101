# Search a text file with regex

Rust example code to search a text file by using the `regex` crate for pattern matching.

```rust
use std::fs::File;
use std::io::{BufRead, BufReader};
use regex::Regex;

fn search_file(filename: &str, pattern: &str) -> std::io::Result<Vec<String>> {
    let reader = BufReader::new(File::open(filename)?);
    let re = Regex::new(pattern)?;
    let mut matches = Vec::new();
    for line in reader.lines() {
        let line = line?;
        if re.is_match(&line) {
            matches.push(line);
        }
    }
    Ok(matches)
}

fn main() -> std::io::Result<()> {
    let filename = "example.txt";
    let pattern = r"\b\d{3}-\d{2}-\d{4}\b"; // Regex to match
    let matches = search_file(filename, pattern)?;
    println!("Found {} matches:", matches.len());
    for line in matches {
        println!("{}", line);
    }
    Ok(())
}
```

This code defines a function `search_file` that takes a filename and a regular expression pattern as input, and returns a vector of matching lines in the file. The function reads the file line by line using a `BufReader`, and uses the regex `is_match` method to test each line against the pattern. If a line matches, it is added to the `matches` vector. The function returns the vector.

In the main function, we call `search_file` with a filename and a regular expression pattern, and then print the matching lines to the console. This code assumes that the file exists and can be opened for reading, and that the pattern is well-formed.
