# redis
* Remote Dictionary Server, is a fast, open-source, in-memory key-value data store for use as a database, cache, message broker, and queue.
* Redis now delivers sub-millisecond response times enabling millions of requests per second for real-time applications in Gaming, Ad-Tech, Financial Services, Healthcare, and IoT. Redis is a popular choice for caching, session management, gaming, leaderboards, real-time analytics, geospatial, ride-hailing, chat/messaging, media streaming, and pub/sub apps
* All Redis data resides in-memory, in contrast to databases that store data on disk or SSDs. By eliminating the need to access disks, in-memory data stores such as Redis avoid seek time delays and can access data in microseconds
* Redis and MemCached are in-memory, open-source data stores. Memcached, a high-performance distributed memory cache service, is designed for simplicity while Redis offers a rich set of features that make it effective for a wide range of use case
* All Redis data resides in the server’s main memory, in contrast to databases such as PostgreSQL, Cassandra, MongoDB and others that store most data on disk or on SSDs. In comparison to traditional disk based databases where most operations require a roundtrip to disk, in-memory data stores such as Redis don’t suffer the same penalty. They can therefore support an order of magnitude more operations and faster response times. The result is – blazing fast performance with average read or write operations taking less than a millisecond and support for millions of operations per second.
* Strings – text or binary data up to 512MB in size
* Lists – a collection of Strings in the order they were added
* Sets – an unordered collection of strings with the ability to intersect, union, and diff other Set types
* Sorted Sets – Sets ordered by a value
* Hashes – a data structure for storing a list of fields and values
* Bitmaps – a data type that offers bit level operations
* HyperLogLogs – a probabilistic data structure to estimate the unique items in a data set
* Redis simplifies your code by enabling you to write fewer lines of code to store, access, and use data in your applications
* Redis employs a primary-replica architecture and supports asynchronous replication where data can be replicated to multiple replica servers.
* Redis offers a primary-replica architecture in a single node primary or a clustered topology. This allows you to build highly available solutions providing consistent performance and reliability. When you need to adjust your cluster size, various options to scale up and scale in or out are also available. This allows your cluster to grow with your demands
* Redis is an open source project supported by a vibrant community. There’s no vendor or technology lock in as Redis is open standards based, supports open data formats, and features a rich set of clients.
# Queue
* A queue is another common data structure that places elements in a sequence, similar to a stack. A queue uses the FIFO method (First In First Out), by which the first element that is enqueued will be the first one to be dequeued
* Enqueue() — Inserts an element to the end of the queue
* Dequeue() — Removes an element from the start of the queue
* isEmpty() — Returns true if queue is empty
* Top() — Returns the first element of the queue

# Task queue overview
* wo different types of task queues. Our first queue
will be built to execute tasks as quickly as possible in the order that they were inserted.
Our second type of queue will have the ability to schedule tasks to execute at some
specific time in the future
# Task queue FIFO
* First-in, first-out queues
* first-in, first-out (FIFO), last-in first-out (LIFO), and priority queues.
We’ll look first at a first-in, first-out queue, because it offers the most reasonable
semantics for our first pass at a queue, can be implemented easily, and is fast.
* By using multiple queues, priorities can be implemented easily. There are situations
* there are many more options for queues in Redis

# BUll quickstart
* Bull is a Node library that implements a fast and robust queue system based on redis.
* Although it is possible to implement queues directly using Redis commands, this library provides an API that takes care of all the low-level details and enriches Redis basic functionality so that more complex use-cases can be handled easily.
* If you are new to queues you may wonder why they are needed after all. Queues can solve many different problems in an elegant way, from smoothing out processing peaks to creating robust communication channels between microservices or offloading heavy work from one server to many smaller workers, etc.
* A queue instance can normally have 3 main different roles: A job producer, a job consumer or/and an events listener.
* Talking about workers, they can run in the same or different processes, in the same machine or in a cluster. Redis will act as a common point, and as long as a consumer or producer can connect to Redis, they will be able to co-operate processing the jobs.
* There are some important considerations regarding repeatable jobs:

Bull is smart enough not to add the same repeatable job if the repeat options are the same. 
If there are no workers running, repeatable jobs will not accumulate next time a worker is online.
repeatable jobs can be removed using the removeRepeatable method.