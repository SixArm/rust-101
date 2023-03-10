# Make HTTP GET request with reqwest crate

Rust example code to make an HTTP GET request to a URL and print the response body, with the `reqwest` crate.

```rust
use reqwest::Error;

async fn make_request(url: &str) -> Result<String, Error> {
    let response = reqwest::get(url).await?;
    let body = response.text().await?;
    Ok(body)
}

#[tokio::main]
async fn main() -> Result<(), Error> {
    let url = "https://www.example.com";
    let response_body = make_request(url).await?;
    println!("{}", response_body);
    Ok(())
}
```

This code defines an asynchronous function `make_request` that takes a URL as input and returns a Result containing the response body as a `String` if the request succeeds. The function uses the `reqwest::get` function to make an HTTP GET request to the specified URL, and then uses the text method of the response object to extract the response body as a string.

In the main function, we call `make_request` with a URL and then print the response body to the console. Note that this code assumes that the URL is valid and that the server responds with a successful HTTP status code. Also, we use `#[tokio::main]` attribute to execute our async main function, as we are using `async-await` in our `make_request` function.
