# cargo-dist crate for distribution archives

<https://crates.io/crates/cargo-dist>

The Rust cargo-dist crate is a Rust crate that provides a simple and convenient way to package a Rust project as a distributable archive. The crate is designed to work with the Rust cargo build system, and provides a number of features that make it easy to create archives for various platforms.

One of the main features of `cargo-dist` is its support for cross-compiling. The crate can automatically build and package your Rust project for a number of different platforms, including Windows, macOS, Linux, and Android, all from a single command. This can save a lot of time and effort when distributing your project to users on multiple platforms.

Another useful feature of `cargo-dist` is its support for packaging dependencies. When you create a distributable archive with `cargo-dist`, it will automatically include all of the dependencies for your Rust project, so users don't have to manually install them. This can help simplify the installation process for your project and reduce the risk of dependency conflicts.

Finally, `cargo-dist` provides a number of options for customizing the packaging process. You can specify the format of the archive (e.g. `.tar.gz`, `.zip`, etc.), include or exclude specific files or directories, and more. This can help ensure that the distributable archive contains exactly what you want, and nothing more.

In summary, the `cargo-dist` crate provides a convenient and flexible way to package your Rust project as a distributable archive, with support for cross-compiling, dependency packaging, and customization options.

TODO: example
