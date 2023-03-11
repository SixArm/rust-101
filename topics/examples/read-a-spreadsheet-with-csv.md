# Read a spreadsheet with CSV

Rust example code to read CSV file, by using the `csv` crate:

```rust
use std::error::Error;
use std::fs::File;
use std::io::prelude::*;
use csv::ReaderBuilder;

fn main() -> Result<(), Box<dyn Error>> {
    let file_path = "data.csv";
    let mut file = File::open(file_path)?;
    let mut contents = String::new();
    file.read_to_string(&mut contents)?;

    let mut reader = ReaderBuilder::new()
        .has_headers(true)
        .delimiter(b',')
        .from_reader(contents.as_bytes());

    for result in reader.records() {
        let record = result?;
        println!("{:?}", record);
    }

    Ok(())
}
```

This code reads a CSV file located at `data.csv`, reads its contents into a string, and then uses the `csv` crate's `Reader` to parse the CSV data. The `has_headers` method specifies that the CSV file contains a header row, and the delimiter method specifies that the field separator is a comma.

The for loop iterates over each record in the CSV file and prints it to the console. Each record is represented as a `csv::StringRecord`, which can be indexed or iterated over to access individual fields. The `?` operator is used throughout the code to handle errors that may occur during file I/O or CSV parsing.
