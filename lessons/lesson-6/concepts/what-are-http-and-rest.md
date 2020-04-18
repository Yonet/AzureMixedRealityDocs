# What are HTTP and REST?

**Hyper-Text Transfer Protocol** (**HTTP**) is a protocol that allows documents and resources to be sent between clients and servers. When a website URL starts with `http` or `https`, that indicates that website is a resource that your web browser will access using the HTTP protocol! We'll talk about alternate protocols a little later, in the [How to have real-time data in your application]() section.

**Representational state transfer** \(**REST**\) is a software architectural style that defines a set of constraints to be used for creating Web services.

HTTP defines the underlying protocol that computers use to communicate over a network, while REST layers on a few conventions to make it easier for different servers and services to interoperate with each other. It's technically possible to use HTTP without using REST, and it's possible to use REST on top of protocols other than HTTP, but you typically see the two used hand-in-hand.

In general, when you make a REST HTTP API call, you need a few things:

1. The URL you want to access.
2. What verb you're using. HTTP defines a series of different commands, and REST enforces that you use them as appropriate. For example, the `GET` verb indicates you're requesting some sort of content (this is what your web browser uses when visiting a website). The other most common verbs you'll see are `POST`, `PUT`, and `DELETE` (to create new resources, to create or update existing resources, and to delete resources, respectively).
3. (Optionally) some headers. These are key-value pairs that let you specify your intent to the server. These are often used for tasks like authenticating who you are by providing some sort of secret key, or specifying what format you want to receive data back in. As an example setting `Content-Type` to `application/json` tells the web server that any data you are sending it is JSON. REST APIs are stateless, meaning the server doesn't have any specific knowledge about the client making the request, so this is typically where you'd include any context you need to.
4. (Optionally) a "body" containing some data. If you're trying to, say, upload an image to a server, here's where you'd include the raw image data.
