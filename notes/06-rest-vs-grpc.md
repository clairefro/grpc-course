## REST vs gRPC

| grpc                        | REST                  |
| --------------------------- | --------------------- |
| protobuff                   | JSON                  |
| http2                       | http1                 |
| streaming support           | unary only            |
| bidirectional communication | client -> server only |
| free design                 | GET/POST/DELETE etc   |

Why use grpc

- codegen
- more secure (serialization, SSL, interceptors for auth)
- streaming support
- API oriented
