---
title : HashMap and HashTable
notetype : feed
date : 29-10-2022
---


`principle` apply hash function to a key and put into a bucket

HashMap and HashTable and ConcurrentHashMap

- **HashMap** is not thread safe. It allows one null key and value. M
	- Modification during iteration gives exception
- **HashTable** is *synchronised*. It doesn't allow null key. 
	- This is an legacy implementation using dictionary for thread safety. modification during iteration gives exception

- **Thread safety** is many threads concurrently accessing a method, class or block of code without an error/corruption in result data
- Synchronisation is one way to achieve thread safety by having a single lock.
- Locking / Reentrant locking provides tryLock, interrupt while requesting for lock method or try lock with a timeout

-   `Collections.synchronizedMap(Map)`

- **ConcurrentHashMap** is a thread safe implementation of HashTable. 
	- ConcurrentHashMap divides the map into **buckets** based on concurrency level (default 16) while HashTable blocks the whole object. 
	- Modification of map during iteration is possible. 
	- Multiple threads can access map at a time
	- It uses implementations like database shards to lock few buckets

`References
- https://stackoverflow.com/questions/510632/whats-the-difference-between-concurrenthashmap-and-collections-synchronizedmap
- https://stackoverflow.com/questions/4201713/synchronization-vs-lock/34267717#34267717
- https://medium.com/javarevisited/comparing-hashmap-and-concurrenthashmap-in-java-e131769c2eec

