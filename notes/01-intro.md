Micro services need to agree on:

- API for data exhcange
- Data format
- Error patterns
- Load balancing

"Building an API is hard"
-> think through endpoints
-> data format tradefoffs (XML vs JSON etc)
-> error handling
-> Auth, monitoring, logging....

gRPC

- free, Opensource framework developed by Google
- modern
- fast
- built on HTTP2
- language agnostic

RPC = remote procedure call

- like calling a function directly on server

How to start

1. choose a supported langauge
2. generate code (protobuff)

example proto file

```proto
syntax = "proto3"
message Greeting {
    string first_name = 1;
}

message GreetRequest {
    Greeting greeting = 1;
}

message GreetResponse {
    string result = 1;
}

service GreetService {
    rpc Greet(GreetRequest) returns (GreetResponse){}
}
```

Why ProtoBuff

- language agnostic
- small payload
- easy API evolution

Why learn gRPC

- many companies/OS projects are using it
- "future of microservices"
- microcontrollers/mobile to server APIs
