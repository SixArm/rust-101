# sqlx crate for SQL databases

<https://crates.io/crates/sqlx>

The Rust sqlx crate is a third-party library that provides a safe and convenient way to interact with databases in Rust. It supports a wide range of database backends, including PostgreSQL, MySQL, SQLite, and Microsoft SQL Server, and provides a high-level API that makes it easy to execute SQL queries and manage database transactions.

To use the sqlx crate in your Rust project, you'll need to add it as a dependency in your Cargo.toml file. Once you've done that, you can start using its functions and macros to interact with your database.

Overall, the `sqlx` crate provides a convenient and efficient way to interact with databases in Rust, making it easy to execute SQL queries, manage transactions, and convert database results into Rust types. It is a popular choice for Rust developers who need to work with databases, and it supports a wide range of database backends, making it suitable for many different uses.


## sqlx query execution

The `sqlx` crate provides a range of functions and macros for executing SQL queries and processing the results. For example, the `query` macro can be used to execute a parameterized SQL query and return the results as a vector of rows:

```rust
use sqlx::{postgres::PgPool, Row};

#[derive(Debug)]
struct Person {
    id: i32,
    name: String,
}

#[async_std::main]
async fn main() -> Result<(), sqlx::Error> {
    let pool = PgPool::new("postgres://user:password@localhost/mydb").await?;
    let rows = sqlx::query_as::<_, Person>("SELECT id, name FROM person WHERE age > $1")
        .bind(18)
        .fetch_all(&pool)
        .await?;

    for row in rows {
        println!("Person: {:?}", row);
    }

    Ok(())
}
```


## sqlx transactions

The `sqlx` crate provides a simple and safe way to manage database transactions, using the `begin`, `commit`, and `rollback` functions. For example, you can use these functions to perform a database update within a transaction:

```rust
use sqlx::{postgres::PgPool, Transaction};

#[async_std::main]
async fn main() -> Result<(), sqlx::Error> {
    let pool = PgPool::new("postgres://user:password@localhost/mydb").await?;
    let mut tx = pool.begin().await?;

    sqlx::query("UPDATE person SET name = $1 WHERE id = $2")
        .bind("Alice")
        .bind(1)
        .execute(&mut tx)
        .await?;

    tx.commit().await?;

    Ok(())
}
```


## sqlx type conversion

The `sqlx` crate provides automatic type conversion for many Rust types, including integers, strings, and dates. For example, you can use the `query_as` function to automatically convert query results into a custom struct:

```rust
use sqlx::{postgres::PgPool, Row};

#[derive(Debug)]
struct Person {
    id: i32,
    name: String,
    age: i32,
}

#[async_std::main]
async fn main() -> Result<(), sqlx::Error> {
    let pool = PgPool::new("postgres://user:password@localhost/mydb").await?;
    let row = sqlx::query("SELECT id, name, age FROM person WHERE id = $1")
        .bind(1)
        .fetch_one(&pool)
        .await?;

    let person = Person {
        id: row.get(0),
        name: row.get(1),
        age: row.get(2),
    };

    println!("Person: {:?}", person);

    Ok(())
}
```
