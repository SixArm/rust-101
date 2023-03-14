# tonic crate for gRPC

The Rust tonic crate is a popular asynchronous gRPC framework that enables developers to quickly build high-performance and scalable client and server applications using Rust programming language. 

gRPC is an open-source, high-performance Remote Procedure Call (RPC) framework. It is designed to be efficient and lightweight and uses Protocol Buffers for serialization, which can give 10 times faster performance over REST with JSON. gRPC allows two services to communicate with each other across different languages and platforms.

The tonic crate provides a set of tools for creating and managing gRPC-based APIs, with support for streaming, bidirectional communication, and response compression. Features also include load balancing, custom metadata, authentication, and health checking. It uses asynchronous programming concepts to enable efficient handling of large numbers of concurrent user requests, making it ideal for building real-time communication applications.

The Rust tonic crate is built on top of the Tokio runtime, which provides a high-performance, asynchronous, event-driven architecture that enables Rust applications to run efficiently and reliably. It also supports a range of programming languages and platforms, including C++, Python, Java, and .NET, making it a versatile solution for building cross-platform applications.

Overall, the Rust tonic crate is an excellent choice for developers looking to build high-performance, concurrent, and scalable gRPC applications in Rust. Its ease of use and support for modern programming paradigms make it an excellent choice for building complex systems with ease.

<div style="page-break-before:always"></div>

## tonic crate example of a gRPC server

```rust
use tonic::{transport::Server, Request, Response, Status};

pub mod greeter {
    tonic::include_proto!("greeter");

    #[derive(Default)]
    pub struct MyGreeter {}

    #[tonic::async_trait]
    impl Greeter for MyGreeter {
        async fn say_hello(&self, request: Request<HelloRequest>) -> Result<Response<HelloReply>, Status> {
            println!("Got a request from {:?}", request.remote_addr());

            let reply = HelloReply {
                message: format!("Hello, {}!", request.get_ref().name),
            };

            Ok(Response::new(reply))
        }
    }
}

#[tokio::main]
async fn main() -> Result<(), Box<dyn std::error::Error>> {
    let addr = "[::1]:50051".parse()?;

    let greeter = greeter::MyGreeter::default();

    println!("Server listening on {:?}", addr);

    Server::builder()
        .add_service(GreeterServer::new(greeter))
        .serve(addr)
        .await?;

    Ok(())
}
```


<div style="page-break-before:always"></div>

## tonic crate example of a gRPC client

```rust
use tonic::transport::Channel;
use greeter::greeter_client::GreeterClient;
use greeter::{HelloReply, HelloRequest};

#[tokio::main]
async fn main() -> Result<(), Box<dyn std::error::Error>> {
    let channel = Channel::from_static("http://[::1]:50051")
        .connect()
        .await?;

    let mut client = GreeterClient::new(channel);

    let request = HelloRequest {
        name: "World".into(),
    };

    let response = client.say_hello(request).await?;

    println!("Got response: {:?}", response);

    Ok(())
}
```
