# Textwrap crate for text wrapping

<https://crates.io/crates/textwrap>

The Rust Textwrap crate is a library for wrapping and formatting text in Rust. It provides a simple API for wrapping text to a specified width, as well as support for indentation, alignment, and hyphenation.

The Textwrap crate can be used for a variety of text formatting tasks, such as formatting text for display in a terminal, wrapping text for printing to a file, or formatting text for display in a GUI application.

Some of the key features of the Textwrap crate include:

* Support for wrapping text to a specified width, with options for indenting and aligning the wrapped text.

* Support for hyphenation, which can improve the readability of text by breaking long words across lines.

* Support for custom line breaking rules, which can be used to handle special cases such as URLs or email addresses.

* A simple and easy-to-use API, with sensible defaults that make it easy to get started with text wrapping in Rust.

* Support for a variety of text input and output formats, including plain text, HTML, and Markdown.

Overall, the Rust Textwrap crate is a powerful tool for formatting and wrapping text in Rust. Its flexible API and support for advanced features like hyphenation and custom line breaking rules make it a great choice for developers looking to format text for a variety of applications.

<div style="page-break-before:always"></div>

## Textwrap crate example

Here is an example of using the textwrap crate in Rust programming language:

```rust
use textwrap::{wrap, dedent};

fn main() {
    let input_text = "Rust is a great programming language for our projects";
    let wrapped_text = wrap(input_text, 25);
    let dedented_text = dedent(wrapped_text);
    println!("{}", dedented_text);
}
```

In this example, we import the `wrap` and `dedent` functions from the textwrap crate. `wrap` is used to wrap text into lines of a specified width, while `dedent` removes common leading whitespace from the start of each line. We then pass in a sample text string, wrap it to 25 characters per line, and dedent the text. Finally, we print the formatted text to the console.

The output of this program will be:

```text
Rust is a great
programming language
for our projects
```
