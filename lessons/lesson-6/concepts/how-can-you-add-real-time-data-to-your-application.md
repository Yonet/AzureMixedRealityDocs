# How can you add real-time data to your application?

HTTP and REST APIs are very powerful, but they also have a bit of an overhead. Every time you make a request to a server, the HTTP protocol requires a bunch of extra communication and handshaking before the data itself can be sent. Because HTTP requests are stateless, every time you make an HTTP request, your application has to negotiate this with the server like it's the first time the two of them have ever communicated. As a result, your average HTTP request might take anywhere from a few hundred milliseconds to a few seconds to complete.

For many API requests, that's fine. But if you're trying to build out something like a real-time multiplayer experience, that's way too slow!

There are a number of lower-latency ways to communicate over a network that depend on what you're trying to do.

For situations where you want something simple, Websockets are a great

you can use to communicate with a server, or directly with other Mixed Reality devices using peer-to-peer technology. With web applications, you'll often see WebSockets used, a technology that BLAH.

For traditional multiplayer games, you'll often see
