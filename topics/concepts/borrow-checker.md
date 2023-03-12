# Borrow checker

The Rust borrow checker is a tool that ensures memory safety in Rust programs by preventing data races and other forms of undefined behavior related to memory management. In Rust, memory is managed through a system of ownership and borrowing, where ownership represents exclusive control over a piece of memory, and borrowing represents temporary access to that memory.

When a variable is created in Rust, it becomes the owner of the memory it represents. The owner is responsible for freeing the memory when the variable goes out of scope. However, Rust also allows you to borrow references to the memory owned by another variable, but with certain constraints. The borrow checker enforces these constraints to prevent invalid memory access and data races.

The borrow checker analyzes Rust code to ensure that each reference to memory is valid and safe. It enforces a set of rules that govern how and when references can be created, used, and dropped. These rules include:

* Only one mutable reference to a piece of memory can exist at a time.

* Mutable references can't coexist with immutable references to the same piece of memory.

* References must always be valid and non-null.

* The lifetime of a reference must be shorter than the lifetime of the memory it refers to.

The borrow checker is an important part of Rust's memory safety guarantees and has become one of the most notable features of the language. It can be challenging to work with at first, especially for developers coming from languages without similar constraints, but it ultimately helps catch many memory-related bugs at compile time rather than at runtime.

<div style="page-break-before:always">&nbsp;</div><p></p>

## Borrow checker example

```rust
struct MyStruct {
    data: Vec<i32>
}

impl MyStruct {
    fn add_data(&mut self, num: i32) {
        self.data.push(num);
    }
    fn get_data(&self) -> &Vec<i32> {
        &self.data
    }
}

fn main() {
    let mut my_struct = MyStruct { data: vec![1, 2, 3] };
    
    // Invalid because `my_struct` is already mutably borrowed:
    //let borrow1 = &mut my_struct;
    
    // Invalid because `my_struct` is already mutably borrowed:
    //let borrow2 = &my_struct;
    
    my_struct.add_data(4);
    
    // Invalid because `my_struct` is already mutably borrowed:
    //println!("The first value is: {}", my_struct.data[0]);
    
    let borrow1 = &mut my_struct;
    
    // Invalid because `my_struct` is already borrowed:
    //let borrow2 = &my_struct;
    
    borrow1.add_data(5);
    
    // Invalid because `borrow1` is mutably borrowed:
    //my_struct.add_data(6);
    
    let borrow2 = &my_struct;
    
    // Invalid because `borrow1` is mutably borrowed:
    //borrow1.add_data(7);
    
    println!("The data in my_struct is: {:?}", borrow2.get_data());
}
```

In this example, we have a simple struct `MyStruct` that has a `Vec` of integers. We define two methods on this struct - `add_data` which adds a new integer to the `Vec`, and `get_data` which returns a reference to the `Vec`. 

In the `main` function, we create an instance of `MyStruct` and add a new integer to it using the `add_data` method. Next, we create a mutable borrow of `my_struct` using the `&mut` operator and assign it to `borrow1`. We are then able to call the `add_data` method on `borrow1` to add another integer to the `Vec`. 

Next, we create an immutable borrow of `my_struct` using the `&` operator and assign it to `borrow2`. We can then call the `get_data` method on `borrow2` to print out the contents of the `Vec`.

However, if we try to borrow `my_struct` immutably before the mutable borrow `borrow1` is dropped, the code will fail to compile. This is because the Rust borrow checker ensures that references to a mutable value are not held at the same time as references to the same value as immutable.
