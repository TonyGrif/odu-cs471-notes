---
tags:
  - Process
---
# Threads
A thread represents a unit of execution for a [[Process Overview | process]]. It consists of a program counter, stack, set of registers, and a unique thread ID. Threads are utilized to simultaneously perform tasks that can be performed independently from each other.
## Multi-Threading
This occurs when a [[Process Overview | process]] contains multiple threads that share common code, data, and certain structures specific to the program. 
### Benefits
1. Responsiveness: can utilize threads to perform quick actions and leave others to do the heavy computation.
2. Resource Sharing: allows multiple tasks to be performed simultaneously in a single address space.
3. Economy: creating and managing threads is faster than creating and managing processes.
4. Scalability: can split among multiple processors.
### Thread Models
Multi-thread contains two types of threads managed in an operating system:
1. User Threads: supported without kernel support, where application programmers would put their programs.
2. Kernel Threads: supported by the kernel itself.
#### Mapping
In a specific implementation, user threads must be mapped to kernel threads. This can be done through any of the following methods:
1. Many-To-One: many user threads are mapped to a single kernel thread.
    1. Very efficient.
    2. System blocking calls block all threads, even if they could otherwise continue.
    3. Unable to be split among multiple CPUs.
2. One-To-One: one user thread mapped to one kernel thread.
    1. Greater overhead.
    2. Can split among multiple CPUs.
3. Many-To-Many: multiplexes any number of user threads to an equal or lesser number of kernel threads.
    1. Combines best features of the two above.
    2. Blocking kernel system calls do not block entire process.
    3. Can be split among multiple CPUs.