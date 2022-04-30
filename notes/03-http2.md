## HTTP/2

http/2 vs http/1.1

- http/2 is faster

## HTTP 1

Why HTTP1 is slow:

- 1 TCP connection **per request**
  -> open connection, request `restaurants`, wait for response, close connection
- Plaintext headers (= bigger payload)
- Only accepts request/response pattern
- Requires GET/POST etc verbs

each website we vist, we load avg of 80 assets

CLIENT <=> SERVER
need to get HTML, CSS and JS

1. open tcp connection and get html
1. open tcp connection and get css
1. open tcp connection and get js

## HTTP2

more efficient

- 1 TCP connection (long lasting) for mulitple requests
- server push (server can give client all the assets it needs when the data is ready, no need for multiple reqs)
- multiplexing: server and client can push messages in parallel
- payloads (headers and data) are binary
- SSL required (more secure by default)

CLIENT <=> SERVER

1. open tcp connection, get html, css, js back from server

(less overhead)

- less chatter
- less bandwith
- more secure
- all for free w/ grpc framework
