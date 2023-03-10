# Access a SQLite database 

Rust example code to access a SQLite database.

First, add the rusqlite crate to your project's dependencies in the Cargo.toml file:

```rust
[dependencies]
rusqlite = "*"
```

Connect to a SQLite database and execute SQL queries like this:

```rust
use rusqlite::{Connection, Result};

fn main() -> Result<()> {
    let conn = Connection::open("example.db")?;

    // Create a table
    conn.execute(
        "CREATE TABLE IF NOT EXISTS people (
                  id              INTEGER PRIMARY KEY,
                  name            TEXT NOT NULL,
                  age             INTEGER NOT NULL
                  )",
        [],
    )?;

    // Insert some data
    conn.execute(
        "INSERT INTO people (name, age) VALUES (?1, ?2)",
        ["Alice", 42],
    )?;

    // Query the data
    let mut stmt = conn.prepare("SELECT name, age FROM people")?;
    let rows = stmt.query_map([], |row| {
        Ok((row.get::<_, String>(0)?, row.get::<_, i32>(1)?))
    })?;

    for row in rows {
        println!("Name: {}, Age: {}", row.unwrap().0, row.unwrap().1);
    }

    Ok(())
}
```

In this example, we're creating a `Connection` to a SQLite database file named `example.db`, creating a table named people, inserting some data into it, and then querying the data and printing it out. The rusqlite library provides many other features for working with SQLite databases, such as transactions, prepared statements, and more.
