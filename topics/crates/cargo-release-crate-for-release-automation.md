# cargo-release crate for release automation

<https://crates.io/crates/cargo-release>

The Rust cargo-release crate is a third-party library that provides a set of tools for releasing Rust crates to repositories like crates.io. It automates many of the steps involved in releasing a new version of a crate, making it easier and more efficient to manage the release process.

To use the `cargo-release` crate in your Rust project, you'll need to add it as a dependency in your `Cargo.toml` file. Once you've done that, you can configure the crate by creating a `.cargo` directory in your project root and adding a `config.toml` file with the following contents:

```toml
[package]
version = "0.1.0"

[dependencies]
cargo-release = { version = "0.15", features = ["procmacro"] }

[release]
# ... configure release options here ...
```

Overall, the `cargo-release` crate provides a powerful and flexible set of tools for managing the release process for Rust crates. It can help to streamline the release process, reduce the risk of errors and inconsistencies, and ensure that your crates are published to repositories like crates.io in a consistent and reliable manner.


## cargo-release features and functions

Here are some of the features and functions provided by the cargo-release crate:

Release Management: The `cargo-release` crate provides a range of tools for managing the release process, including the ability to automatically generate a new version number based on a specified release type (e.g. major, minor, or patch), update the changelog and version number in your crate's Cargo.toml file, tag the release in Git, and publish the crate to crates.io:

```bash
cargo release --dry-run  # preview the release process
cargo release            # perform the release
```

Pre-Release Management: The `cargo-release` crate also provides tools for managing pre-releases, including the ability to create and publish pre-release versions of your crate (e.g. 0.2.0-alpha.1), and to promote pre-release versions to stable releases:

```bash
cargo release --pre-release  # create a pre-release version
cargo release --continue     # promote a pre-release to stable
```

Customization: The `cargo-release` crate is highly configurable, allowing you to customize the release process to suit your needs. For example, you can specify which branches to release from, configure the changelog format and location, and specify additional steps to perform during the release process:

```toml
[release]
branches = ["main"]
changelog = "docs/CHANGELOG.md"
pre-release = false

[release.steps.post]
# ... additional steps to perform after the release ...
```
