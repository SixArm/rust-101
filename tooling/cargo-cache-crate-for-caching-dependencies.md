# cargo-cache crate for caching dependencies

Rust `cargo-cache` is a crate that provides a command-line interface (CLI) for managing the cache directory used by the Cargo package manager. Cargo is the default package manager for Rust and is used to build, test, and package Rust code.

When you use Cargo to build a Rust project, it downloads and caches dependencies, build artifacts, and other files related to the build process in a directory called "cargo-cache". Over time, this directory can become quite large, taking up valuable disk space on your system.

The `cargo-cache` crate provides several commands that allow you to manage the cache directory. Some of the key features of cargo-cache include:

* Listing the contents of the cache directory

* Clearing the cache directory

* Showing the size of the cache directory

* Displaying information about individual cached packages

Using `cargo-cache`, you can easily clear out old or unnecessary cached files, reclaiming valuable disk space on your system. You can also use the `cargo-cache` CLI to better understand the contents of the cache directory and diagnose any issues related to the build process.

In summary, `cargo-cache` is a helpful tool for managing the cache directory used by the Cargo package manager in Rust projects.
