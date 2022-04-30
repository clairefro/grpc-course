## Protobuff

gRPC using protocal buffers (protobuff)

Why?

- efficiency over JSON (smaller payload)

JSON 52 bytes (compressed)

```json
{
  "age": 26,
  "first_name": "Clement",
  "last_name": "JEAN"
}
```

Proto **17 bytes**

```proto
syntax = "proto3"

message Person {
    uint32 age = 1;
    string first_name = 2;
    string last_name = 3;
}
```

JSON is CPU intensive bc format is human readable

Proto is less CPU intensive bc it is binary

## Supported gRPC languages

https://grpc.io/docs/languages/
(more langauge are support by community, like Swift for iOS)

Pure implementations: Java, Go, C

Derivative implementations (from C): C++, Python, C#...

\*Derivative implementations are downstream, meaning it will take longer for updates to grpc to cascade down

Protobuff will generate code for you

efficient serialization/deserialization due to low CPU intensity (binary)
