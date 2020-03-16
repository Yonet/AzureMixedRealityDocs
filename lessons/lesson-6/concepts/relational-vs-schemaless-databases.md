# Relational vs schemaless databases

The most "traditional" databases are known as relational databases. Here, you need to specify your database's structure ahead of time. These are incredibly robust — fast, powerful, feature-filled, scalable — but if you need to adjust the type of data you're storing in your database, they can be a pain to work with, which can make them frustrating when working on prototypes and small projects where you're figuring out the shape of your data as you go.

The alternative is "NoSQL" databases, so called because they don't require you to write database queries in the "SQL" query language. They're generally schemaless, meaning you don't need to specify a structure ahead of time. You can essentially just put JSON objects into them, and still perform complex queries on the data contained within that JSON. Schemaless databases are traditionally more difficult to scale tham relational ones, but can be a lot easier to work with, and give you a lot more flexibility when you're just starting out.

For the project in this chapter, we'll be working with CosmoDB, which is a schemaless database.
