---
tags:
  - Process
---
# Producer-Consumer
This is a classic [[Process Overview | process]] synchronization problem in operating systems. Consumers consumer data from a buffer and producers produce data into the buffer. These entities operate concurrently. The operating system must ensure that the producers do not overproduce and the consumers do not consume the same data from buffer.
## Critical Section
The solution to the producer-consumer problem is to create a critical section, wherein, all operations in this section are uninterruptible (**atomic**). There are a variety of methods to implement this, but all should guarantee:
1. **Mutual Exclusion**: only one process can operate in the critical section at a time.
2. **Progress**: if no process is executing in the CS and there exists a process desires entry to the CS, the selection of the covetous process cannot be postponed indefinitely.
3. **Bounded Waiting**: a bound must exist on the number of times other processes can enter their CS after a process has made a request to enter theirs and before that request is granted.