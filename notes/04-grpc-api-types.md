## types

### Unary

Closest to REST

1. client send a request
1. server sends a response

### Server streaming

1. client send a request
1. server sends one or more response

(ex: getting realtime list updates)

### client streaming

1. client send multiple requests
1. server sends one response

(ex: uploading data, or realtime updates)

### bi-directional streaming

1. client send multiple requests
1. server sends multiple responses

after first request, the responses can arrive in any order (async)

(ex: uploading data, or realtime updates)

## Protobuff representation

notice location of `stream` keyword

```proto
service GreetService {
    // unary
    rpc Greet(GreetRequest) returns (GreetResponse) {};

    // server streaming
    rpc GreetManyTimes(GreetRequest) returns (stream GreetResponse) {};

    // client streaming
    rpc LongGreet(stream GreetRequest) returns (GreetResponse) {};

    // bi-directional streaming
    rpc GreetEveryone(stream GreetRequest) returns (stream GreetResponse) {};
}
```
