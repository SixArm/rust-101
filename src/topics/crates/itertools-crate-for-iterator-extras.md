
# itertools crate for iterator extras

<https://crates.io/crates/itertools>

The Rust itertools crate is a third-party library that provides a powerful set of tools for working with iterators in Rust. It offers a wide range of functions and macros for manipulating and combining iterators, making it easier and more efficient to work with collections of data in Rust.

To use the itertools crate in your Rust project, you'll need to add it as a dependency in your `Cargo.toml` file. Once you've done that, you can import the crate and start using its functions and macros.

Iteration Functions: The itertools crate provides functions that can be used to manipulate and transform iterators. For example, the enumerate function adds an index to each element of an iterator, while the zip function combines multiple iterators into a single iterator of tuples:

```rust
use itertools::Itertools;

let numbers = vec![1, 2, 3];
let letters = vec!['a', 'b', 'c'];

for (i, (n, l)) in numbers.iter().enumerate().zip(letters.iter()) {
    println!("{}: {}{}", i, n, l);
}
```

Combinator Functions: The itertools crate provides functions that can be used to generate new iterators from existing iterators. For example, the product function generates the Cartesian product of two iterators, while the permutations function generates all possible permutations of an iterator:

```rust
use itertools::Itertools;

let numbers = vec![1, 2];
let letters = vec!['a', 'b'];

for (n, l) in numbers.iter().cartesian_product(letters.iter()) {
    println!("{}{}", n, l);
}

for p in letters.iter().permutations(2) {
    println!("{:?}", p);
}
```

Macros: The itertools crate also provides macros that can be used to simplify the code required to work with iterators. For example, the `assert_equal` macro can be used to test that two iterators are equal, while the `join` macro can be used to concatenate multiple iterators into a single iterator:

```rust
use itertools::assert_equal;
use itertools::join;

let numbers = vec![1, 2, 3];
let squares = vec![1, 4, 9];

assert_equal(numbers.iter().map(|x| x * x), squares.iter());

let lists = vec![vec![1, 2], vec![3, 4], vec![5, 6]];
let flattened = join(lists.iter());

assert_equal(flattened, vec![1, 2, 3, 4, 5, 6].iter());
```

Overall, the itertools crate provides a powerful and flexible set of tools for working with iterators in Rust, making it easier and more efficient to manipulate and transform collections of data.
