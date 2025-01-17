# WTF is RPC??
In [distributed computing](https://en.wikipedia.org/wiki/Distributed_computing "Distributed computing"), a **remote procedure call** (**RPC**) is when a [computer program](https://en.wikipedia.org/wiki/Computer_program "Computer program") causes a [procedure](https://en.wikipedia.org/wiki/Procedural_programming "Procedural programming") (subroutine) to execute in a different [address space](https://en.wikipedia.org/wiki/Address_space "Address space") (commonly on another computer on a shared [computer network](https://en.wikipedia.org/wiki/Computer_network "Computer network")), which is written as if it were a normal (local) procedure call, without the [programmer](https://en.wikipedia.org/wiki/Programmer "Programmer") explicitly writing the details for the remote interaction

* In a normal backend you have routes and controllers now the client can be able to call these controllers as if it were one application. 
* Runs on top of HTTP2
* slower bundle size compared to graphQL but still cant get specific resources
* uses Protocol Buffers to encode and send data over the wire by default(grpc
* Structure of data over the wire is defined in a proto file
* grpc service is also defined in a proto file by specifying RPC method parameters and return types
* Not all browser support
* 