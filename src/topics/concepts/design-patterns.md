# Design patterns

Design patterns are reusable solutions to common programming problems. They are not unique to Rust, but Rust developers can use many of the same design patterns found in other languages. Here are some examples of design patterns.


## Iterator

The iterator pattern provides a way to iterate over a collection of objects. In Rust, this is built into the language with the Iterator trait.

```rust
let numbers = vec![1, 2, 3, 4, 5];
for number in numbers.iter() {
    println!("{}", number);
}
```

## Singleton

The singleton pattern ensures that only one instance of a particular object is ever created. In Rust, this can be implemented using a static variable or a lazy static variable.

```rust
struct Singleton;

impl Singleton {
    fn instance() -> &'static Self {
        static mut INSTANCE: *const Singleton = 0 as *const Singleton;
        static ONCE: Once = Once::new();
        unsafe {
            ONCE.call_once(|| {
                let singleton = Singleton {};
                INSTANCE = mem::transmute(Box::new(singleton));
            });

            &*INSTANCE
        }
    }
}
```


<div style="page-break-before:always"></div>

## Builder design pattern

The builder design pattern creates complex objects by providing a series of simpler steps:

```rust
struct Person {
    name: String,
    age: u32,
}

struct PersonBuilder {
    name: Option<String>,
    age: Option<u32>,
}

impl PersonBuilder {
    fn new() -> Self {
        PersonBuilder {
            name: None,
            age: None,
        }
    }

    fn name(mut self, name: String) -> Self {
        self.name = Some(name);
        self
    }

    fn age(mut self, age: u32) -> Self {
        self.age = Some(age);
        self
    }

    fn build(self) -> Person {
        Person {
            name: self.name.expect("Name not provided"),
            age: self.age.expect("Age not provided"),
        }
    }
}

let person = PersonBuilder::new()
    .name(String::from("John"))
    .age(30)
    .build();
```

<div style="page-break-before:always"></div>

## Observer design pattern

The observer design pattern allows one object to notify others of its state changes. In Rust, this can be implemented using Rust's channels or event emitters. For example:

```rust
use std::sync::mpsc::channel;
use std::thread;

fn main() {
    let (tx, rx) = channel();

    thread::spawn(move || {
        tx.send("Hello, world!").unwrap();
    });

    let message = rx.recv().unwrap();
    println!("{}", message);
}
```
