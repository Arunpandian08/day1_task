# Some major difference of HTTP/1.1 vs HTTP/2
---


**HTTP (Hypertext Transfer Protocol)**:

HTTP is the underlying protocol of the world wide web, developed by ***"Tim Berners-lee"*** and ***team*** between 1989–1991. **HTTP** has gone through many changes that have helped maintain its simplicity while shaping its flexibility.

### Invention of the world wide web:

+ In 1989, Tim Berners-Lee wrote a proposal to build a hypertext system over the internet.
  + Initially its called the '_Mesh_' it was later renamed the world wide web during its implementation in 1990.
  + They build over the existing ***TCP***(transmission control protocol) and IP protocols, it consisted of 4 building blocks.
  + A text format, which represent hypertext documents in ***HTML***(Hypertext Markup language).
  + A simple protocol to exchange there documents in ***HTTP*** (Hypertext transfer protocol).
  + A client to display these documents the first web browser is called the world wide web.
  + A server to give access to the document an early version of **HTTPD**.

---

Evaluation of ***HTTP***:
>> The first evaluation get 1991–1995 ,which is a dubbed **HTTP/0.9** , This is called "_one line protocol_". The initial version of **HTTP** had no version number.

>> ***HTTP/1.0*** ==> Building extensibility [Ref.link](https://datatracker.ietf.org/doc/html/rfc1945)

>> ***HTTP/1.1*** ==> The standardized protocol and its being morethan 15 years of extensions.[Ref.link](https://datatracker.ietf.org/doc/html/rfc2068)

>>***HTTP/2*** ==> A protocol for greater performance. 

>>***Post*** ==> HTTP/2 evolution. 

>>***HTTP/3*** ==> HTTP over QUIC 

Lets see some difference of HTTP/1.1 and HTTP/2;

### HTTP/1.1:
+ It works on the textual format.
+ There is a head of line blocking that blocks all the requests behind if untill it doesn't get its all resources.
+ Its compressed data itself.

### HTTP/2:
+ It works on the binary protocol.
+ It allows multiplexing so one ***TCP*** connection is required for multiple requests.
+ It uses ***HPACK*** for data compression.

now, Lets see brief;

## Multiplexing:
+ ***http/1.1*** loads resources one after the other, so if one resourse cannot be loaded, it blocks all other resources behind it, but In ***http/2*** is able to use a single ***TCP***(Transfer control protocol) connection to send multiple streams of data at once. So that resource blocks any other resource.

## Server push:
 Typically, a server only servers content to a client device if the client asks for it. Whenever, this approach is not practical for modern web pages, but ***HTTP/2*** solves this problem by allowing a server to "push" content to a client before the client asks for it.

## Header compression:
 Small files load more quickly than large ones. To speed up web performance, both ***HTTP/1.1*** and ***HTTP/2*** ,compress HTTP messages to make them smaller and ***HTTP/2*** uses a more advanced compression method is called HPACK that eliminates redundant information in HTTP header packets. This eliminates a few bytes from every HTTP packet.
