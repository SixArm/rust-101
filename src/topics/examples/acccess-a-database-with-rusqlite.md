# Access a database with rusqlite

Rust example code to access a SQLite database, by using the `rusqlite` crate.

Connect to a SQLite database and execute SQL queries like this:

```rust
use rusqlite::{Connection, Result};

fn main() -> Result<()> {
    let conn = Connection::open("example.db")?;

    // Create a table
    conn.execute(
        "CREATE TABLE IF NOT EXISTS people (
            id    INTEGER PRIMARY KEY,
            name  TEXT NOT NULL
        )",
        [],
    )?;

    // Insert some data
    conn.execute(
        "INSERT INTO people (name) VALUES (?1)", ["Alice"],
    )?;

    // Query the data
    let mut stmt = conn.prepare("SELECT name FROM people")?;
    let rows = stmt.query_map([], |row| {
        Ok((row.get::<_, String>(0)?))
    })?;

    for row in rows {
        println!("Name: {}", row.unwrap().0);
    }

    Ok(())
}
```

This example creates a `Connection` to a SQLite database file named `example.db`, creates a table named "people", inserts data into it, queries the data, and prints it out. The rusqlite library provides many other features for working with SQLite databases, such as transactions, prepared statements, and more.
