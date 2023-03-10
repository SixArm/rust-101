# Run a terminal program with cursive

Rust example code to create a simple interactive terminal program, by using the `cursive` crate.

```rust
use cursive::Cursive;
use cursive::views::{Dialog, TextView};

fn main() {
    let mut siv = Cursive::default();

    siv.add_layer(
        Dialog::around(TextView::new("Hello, world!"))
            .title("Cursive Example")
            .button("Quit", |s| s.quit()),
    );

    siv.run();
}
```

This code creates a `Cursive` object, adds a `TextView` containing the message "Hello, world!" to a `Dialog`, and then displays the dialog with a "Quit" button that will close the application when clicked.

Add the `cursive` crate dependency to the `Cargo.toml` file, then you can run this code using `cargo run`.