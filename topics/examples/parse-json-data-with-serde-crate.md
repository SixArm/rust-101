# Parse JSON data

Rust example code to parse a JSON string by using the `serde_json` crate.

```rust
use serde_json::{Result, Value};

fn parse_json(json_string: &str) -> Result<Value> {
    let json: Value = serde_json::from_str(json_string)?;
    Ok(json)
}

fn main() {
    let json_string = r#"
        {
            "name": "John Doe",
            "age": 30,
            "is_employee": true,
            "languages": ["Rust", "Python", "JavaScript"]
        }
    "#;

    let parsed_json = parse_json(json_string).unwrap();

    let name = parsed_json["name"].as_str().unwrap();
    let age = parsed_json["age"].as_u64().unwrap();
    let is_employee = parsed_json["is_employee"].as_bool().unwrap();
    let languages = parsed_json["languages"].as_array().unwrap();

    println!("Name: {}", name);
    println!("Age: {}", age);
    println!("Is Employee: {}", is_employee);
    println!("Languages: {:?}", languages);
}
```

This code defines a function `parse_json` that takes a JSON string and returns a `serde_json::Value` object. The `serde_json::from_str` function is used to parse the JSON string into a `Value` object. The main function demonstrates how to access the values in the parsed JSON by using the `as_*` methods on the `Value` object. In this example, we access the name, age, is_employee, and languages fields of the JSON object and print them to the console. Note that this code assumes that the JSON is well-formed and matches the expected schema.
