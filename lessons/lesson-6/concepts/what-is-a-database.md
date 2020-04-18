# What is a database?

Let's say you have a server that can communicate with your Mixed Reality app. That's great! If your app wants to store some data on the server (say, to share it across users in a multiplayer setting), where should it store that data?

You might assume you can just write it to disk, like you would consider doing with a Unity app, but this doesn't really work well for server-side applications. If your application gets really popular, you'll have a lot of instances of your software reading and writing data at the same time. Even if your application just runs on a single server, this isn't something that accessing files on disk is really good at, but it's also incredibly likely you'll want to scale up to more than one server. Writing to one server's hard disk won't help you if you need to access the same data from a different server!

Databases are pieces of software that are specifically designed to store your data in ways that make it easy to access. Typically, if you have a database that lives on a server, you won't access that database directly from your mixed reality app, as that can pose a security risk. Instead, a database will provide some sort of interface you can access from within your server-side code, and you'll write your own HTTP REST endpoints to expose that data to your mixed reality apps.
