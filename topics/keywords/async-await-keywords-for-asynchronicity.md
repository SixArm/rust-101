# async/await keywords for asynchronicity

Rust provides support for asynchronous programming through its `async`/`await` syntax. The `async` keyword defines a function that can be suspended and resumed later, while the `await` keyword pauses execution of an `async` function until a condition is met.

When a function is declared with the `async` keyword, it becomes an asynchronous function. This means that the function can be paused at any point using the await keyword and resumed later when the awaited value becomes available. The async function returns a `Future` type that represents the result of the computation.

Here's an example of an async function that returns a future:

```rust
async fn fetch_url(url: &str) -> Result<String, reqwest::Error> {
    let response = reqwest::get(url).await?;
    let body = response.text().await?;
    Ok(body)
}
```

In this example, the `fetch_url` function is defined with the `async` keyword. It uses the `reqwest` crate to make an HTTP request. The `await` keyword is used twice to pause the execution of the function until the response is received and the body is retrieved.

The `await` keyword pauses the execution of an `async` function until a condition is met. It can be used with any value that implements the `Future` trait. When `await` is used with a future, it suspends the current task, waits for the future to complete, then returns the result.

Here's an example of using the await keyword to wait for a future:

```rust
async fn do_something() -> i32 {
    let future = get_result_async();
    let result = await!(future);
    result + 1
}
```

In this example, the `await` keyword pauses execution of the `do_something` function until `get_result_async` is completed. Once the future completes, the result is returned and the task is resumed. The value of the result is then incremented by 1 and returned as the final result.