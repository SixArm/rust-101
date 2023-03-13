# arrow-csv crate for loading CSV to Arrow

<https://crates.io/crates/arrow-csv>

The Rust arrow-csv crate is a library that provides support for reading and writing CSV (Comma-Separated Values) files in the Arrow data format in Rust. The Arrow format is a columnar data format that is designed to be efficient and interoperable across different programming languages and systems.

The main types provided by the arrow-csv crate are the `CsvReader` and `CsvWriter` types. The `CsvReader` type represents a CSV reader that can be used to read CSV data from a file or a stream and convert it to an Arrow record batch. The `CsvWriter` type represents a CSV writer that can be used to write Arrow record batches to a CSV file or a stream. Both types support a wide range of options for controlling the CSV parsing and formatting behavior, such as delimiter, quoting, escaping, and encoding.

The arrow-csv crate also provides support for schema inference, which means that it can automatically infer the data types and column names from the CSV data, making it easier to work with CSV files that do not have a predefined schema.

The arrow-csv crate is highly performant and is designed to handle large CSV files efficiently. It provides a range of optimizations, such as parallel processing and memory-mapped files, to minimize memory usage and improve performance.

Overall, the Rust arrow-csv crate is a powerful and efficient library that provides a way to work with CSV data in the Arrow data format in Rust. It is widely used in a variety of applications, including data analysis, data processing, and data exchange.
