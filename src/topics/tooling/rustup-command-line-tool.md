# rustup command-line tool

In Rust, `rustup` is a command-line tool that manages the installation and configuration of Rust toolchains. A Rust toolchain is a set of tools and libraries that are used to compile and run Rust programs.

`rustup` installs and updates Rust toolchains, including the Rust compiler and associated tools such as `cargo`. It also allows for the management of multiple toolchains and makes it easy to switch between them.

Some of the commonly used rustup commands include:

* `rustup install`: Installs a specific version of the Rust toolchain.

* `rustup default`: Sets the default Rust toolchain to use.

* `rustup update`: Updates the Rust toolchain to the latest stable release.

* `rustup self update`: Updates rustup itself to the latest version.

* `rustup component add`: Adds a component to the Rust toolchain, such as a specific target or a specific version of rustfmt.

* `rustup target add`: Adds a new target to the Rust toolchain, such as armv7-unknown-linux-gnueabihf for cross-compiling to an ARM-based Linux system.

* `rustup toolchain list`: Lists all installed Rust toolchains.

* `rustup override`: Sets a toolchain override for a specific directory or project.

`rustup` also allows for the installation of Rust-related components such as the `rust-src` component, which includes the source code for the Rust standard library, or the `rls` component, which provides support for Rust language server integration.

Overall, rustup is a powerful tool that makes it easy to manage Rust toolchains, enabling Rust developers to work with multiple versions of Rust and target different platforms.
