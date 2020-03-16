# Why are there different databases?

Just like you might use different programming languages for different programming tasks, the way your program needs to read and write data will affect what the best tool for the job is. If you're writing a real-time chat app, you need to be able to sling message data around very quickly, and you might have a lot of it, but each individual message's data is going to be very small. On the other hand, a tool that lets people search through a giant archive of legal documents probably doesn't get used as often, and doesn't need to be very fast, but needs to be capable of dealing with vast quantities of data.

There are databases optimized for all sorts of usecases. Do you plan on storing extreme amounts of data? Are you particularly worried about quick access? Are you going to be performing complex queries that need you to be able to compare different pieces of data in interesting ways? No matter what you want to do, there's probably a database that fits your needs.