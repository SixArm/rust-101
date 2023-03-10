# Rustfmt for code formatting

Rustfmt is a code formatting tool for Rust programming language. It automatically reformats Rust code according to a set of predefined formatting rules, which helps developers to maintain consistent coding styles and makes it easier to read, understand and debug the code.

Rustfmt can be used as a standalone tool, or as an integrated feature within a code editor, or via a build script. It supports a variety of formatting options, including indentation style, line wrapping, brace styles, and more.

The tool can be configured by using a `.toml` configuration file, which allows developers to customize the formatting rules according to their preferences.

Using Rustfmt is highly recommended by the Rust community as it helps maintain a consistent coding style across a project, which in turn makes the code easier to read, maintain and understand.

To use Rustfmt, you first need to install it on your system. Rustfmt can be installed using Cargo, the package manager for Rust, by running the following command in your terminal:

```sh
cargo install rustfmt
```

To use Rustfmt as a standalone tool: You can format Rust code using Rustfmt directly from the command line by running the following command:

```sh
rustfmt <filename.rs>
```
This command will format the Rust code in the specified file and print the formatted output to the terminal. If you want to save the formatted output to a file, you can use the -w option followed by the filename, like this:

```sh
rustfmt -w <filename.rs>
```

To use Rustfmt as an integrated feature within a code editor: Rustfmt can be integrated with popular code editors like VSCode, Atom, and Sublime Text. To do this, you need to install a Rustfmt extension for your editor, and then configure it to format your code on save or on demand.

For example, in VSCode, you can install the "Rustfmt" extension and configure it to format your code on save by adding the following line to your `settings.json` file:

```json
"editor.formatOnSave": true
```

This will format your Rust code automatically every time you save a file.

To use Rustfmt via a build script: If you want to format your Rust code as part of your build process, you can use a build script that runs Rustfmt on your code before compiling it. You can create a build script by adding the following line to your `Cargo.toml` file:

```toml
[package]
build = "rustfmt <filename.rs>"
```

This will run Rustfmt on the specified file before compiling your project.

In all cases, you can customize the formatting rules used by Rustfmt by creating a `.toml` configuration file in your project directory and specifying your preferred options. 