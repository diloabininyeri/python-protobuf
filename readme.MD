>Protocol Buffers python exemple client and server 
### What is gRPC?
Quoting the official documentation-

“gRPC or Google Remote Procedure Call is a modern open-source high-performance RPC framework that can run in any environment. It can efficiently connect services in and across data centers with pluggable support for load balancing, tracing, health checking and authentication.”


### Why gRPC? 
- HTTP/2 based transport - It uses HTTP/2 protocol instead of HTTP 1.1. HTTP/2 protocol provides multiple benefits over the latter. One major benefit is multiple bidirectional streams that can be created and sent over TCP connections parallelly, making it swift. 

- Auth, tracing, load balancing and health checking - gRPC provides all these features, making it a secure and reliable option to choose.

- Language independent communication- Two services may be written in different languages, say Python and Golang. gRPC ensures smooth communication between them.

- Use of Protocol Buffers - gRPC uses protocol buffers for defining the type of data (also called Interface Definition Language (IDL)) to be sent between the gRPC client and the gRPC server. It also uses it as the message interchange format. 

Let's dig a little more into what are Protocol Buffers.


### Protocol Buffers
Protocol Buffers like XML, are an efficient and automated mechanism for serializing structured data. They provide a way to define the structure of data to be transmitted. Google says that protocol buffers are better than XML, as they are:

simpler
three to ten times smaller
20 to 100 times faster
less ambiguous
generates data access classes that make it easier to use them programmatically
Protobuf are defined in .proto files. It is easy to define them. 


### Test
unary client
```console
python3 unary_client.py
```

run unary server 
```console
python3 unary_server.py
```
#### Bidirectional server and client
server
```console
python3 bidirectional_server.py
```
client
```console
bidirectional_client.py
```