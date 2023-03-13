# cargo-make crate for task runners

<https://crates.io/crates/cargo-make>

The Rust cargo-make crate is a tool that extends the functionality of the Cargo package manager by providing a way to define complex build processes in a simple, declarative way.

Here are some of the key features of the cargo-make crate:

* Declarative build scripts: With cargo-make, you define your build process in a Toml configuration file, which makes it easy to understand and modify the build process.

* Cross-platform support: cargo-make runs on Linux, macOS, and Windows, making it easy to maintain consistent build processes across different platforms.

* Task management: You can define a set of tasks, each of which can be executed individually or as part of a larger build process.

* Dependency management: cargo-make ensures that tasks are executed in the correct order based on their dependencies, which helps avoid build errors and improve build performance.

* Pre and Post Hooks: cargo-make supports pre and post-hooks which can be used to perform actions before and after the build process, such as cleaning up artifacts, setting environment variables, etc.

* Plugins: cargo-make supports plugins which can be used to extend its functionality, such as adding new tasks or modifying the build process.

To use cargo-make, you first need to install it using the following command:

```sh
cargo install cargo-make
```

After installation, you can define your build process in a Toml configuration file named `Makefile.toml`. 

In summary, `cargo-make` is a powerful tool that simplifies the process of defining and executing complex build processes in Rust. With its declarative configuration, task management, and cross-platform support, cargo-make can help you improve your Rust project's build performance and maintainability.


## cargo-make examples

Here's an example `cargo-make` configuration file `Makefile.toml`:

```toml
[tasks.build]
command = "cargo build --release"

[tasks.test]
command = "cargo test"

[tasks.lint]
command = "cargo clippy"

[tasks.default]
dependencies = ["build", "test", "lint"]
```

In this example, we've defined three tasks: `build`, `test`, and `lint`. Each task has a command that specifies what action to perform when the task is executed. The `default` task depends on the `build`, `test`, and `lint` tasks, and is executed when no task is specified.

You can then run your build process using the following command:

```sh
cargo make
```

This will execute the default task and all its dependencies in the correct order. 

If you want to execute a specific task, you can use the following command:

```sh
cargo make <task-name>
```
