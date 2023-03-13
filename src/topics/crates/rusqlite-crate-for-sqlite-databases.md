# Rusqlite crate for SQLite databases

<https://crates.io/crates/rusqlite>

The Rust Rusqlite crate is a library for working with SQLite databases. It provides many methods for querying and modifying data in SQLite databases, including prepared statements, transactions, and more. 

Here's an example of how to use Rusqlite to create create a table and data:

```rust
use rusqlite::{Connection, Result};

fn main() -> Result<()> {
    let conn = Connection::open("example.db")?;

    conn.execute(
        "CREATE TABLE person (
            id    INTEGER PRIMARY KEY,
            name  TEXT NOT NULL,
            age   INTEGER NOT NULL
        )",
        [],
    )?;

    conn.execute(
        "INSERT INTO person (name, age)
            VALUES (?1, ?2)",
        ["Alice", 30],
    )?;

    Ok(())
}
```

In this example, we first import the `rusqlite` crate and the `Result` type from the standard library, which we'll use to handle errors. We then create a new database connection by calling `Connection::open("example.db")?`, which creates a new SQLite database file called `example.db` in the current directory.

Next, we execute a SQL statement using the `execute()` method. This creates a new table called `person` with three columns: `id`, `name`, and `age`. The `id` column is the primary key for the table, and the `name` and `age` columns are both required.

Finally, we insert a new row into the person table using the `execute()` method again. This inserts a new row with the name "Alice" and the age `30`.

