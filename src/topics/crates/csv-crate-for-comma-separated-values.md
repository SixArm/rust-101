# CSV crate for comma-separated values

<https://crates.io/crates/csv>

The Rust CSV crate is a library for reading and writing CSV (Comma-Separated Values) files in Rust. It provides a fast and efficient way to work with CSV data and supports a wide range of CSV formats and options.

The main types provided by the CSV crate are the `Reader` and `Writer` types. The `Reader` type represents a CSV reader that can be used to read CSV data from a file or a stream. The `Writer` type represents a CSV writer that can be used to write CSV data to a file or a stream. Both types support a wide range of options for controlling the CSV parsing and formatting behavior, such as delimiter, quoting, escaping, and encoding.

The CSV crate also provides a range of other useful types and functions, such as the `ByteRecord` type for representing CSV records as byte arrays, the `StringRecord` type for representing CSV records as UTF-8 strings, and the Serde integration for easy serialization and deserialization of CSV data.

The CSV crate is highly performant and is designed to handle large CSV files efficiently. It provides a range of optimizations, such as lazy parsing and zero-copy parsing, to minimize memory usage and improve performance.

Overall, the Rust CSV crate is a powerful and flexible CSV library that provides a fast and efficient way to work with CSV data in Rust programs. It is widely used in a variety of applications, including data analysis, data processing, and data exchange.

TODO: example
