# CLAP crate for command line arg parsing

<https://crates.io/crates/clap>

The Rust CLAP crate is a popular library for parsing command-line arguments in Rust. It provides a flexible and intuitive way to define command-line interfaces (CLIs) for Rust programs, with support for a wide range of features and options.

To use the CLAP crate in your Rust project, you'll need to add it as a dependency in your `Cargo.toml` file, along with any feature that you want:

```rust
clap = { version = "4", features = ["deprecated", "derive", "cargo", "env", "unicode", "wrap_help", "string"] }
```

Once you've done that, you can import the crate and start defining your CLI options.

Here's a simple example of how to use the CLAP crate to define a CLI for a Rust program, and how to use the `clap::command!` macro:

```rust
use clap::{Arg, ArgAction};

pub fn clap() -> ... {
    let matches = clap::command!()
    .name("My Rust Program")
    .version("1.0.0")
    .author("Alice Adams")
    .about("This is my simple Rust example program")
    .arg(Arg::with_name("input")
        .help("Sets the input file to use")
        .short("i")
        .long("input")
        .action(clap::ArgAction::Set)
    .arg(Arg::new("verbose")
        .help("Set the verbosity level")
        .short('v')
        .long("verbose")
        .action(clap::ArgAction::Count))
    .get_matches();
    if let Some(x) = matches.get_one::<String>("input") {
        println!("Value for --input: {}", x);
    }
    if let Some(x) = matches.get_count("Verbose") {
        println!("Value for --verbose: {}", x);
    }
}
```

In this example, we define a CLI for a program that takes two optional arguments: `--input` and `--verbose`. We use the `clap::command!` macro to define each argument, specifying a help message, a short name, a long names, an an action such as `clap::ArgAction::Set` or `clas::ArgAction::Count`.

We then use the `get_matches()` method to parse the command-line arguments and return a matches struct. We can use this struct to retrieve the values of the `--input` and `--verbose` arguments (if provided).

CLAP offers a variety of syntaxes, such as the macro syntax as above, as well as a `Derive` syntax that can automatically configure many CLAP options, and a builder syntex.

Overall, the CLAP crate provides a powerful and flexible way to parse command-line arguments in Rust, making it easy to build robust and user-friendly command-line interfaces for your Rust programs.
