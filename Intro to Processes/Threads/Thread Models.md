---
tags:
  - Threads
---
# Thread Models
[[Multi-Threading | Multi-thread]] contains two types of threads managed in an operating system:
1. User Threads: supported without kernel support, where application programmers would put their programs
2. Kernel Threads: supported by the kernel itself
## Mapping
In a specific implementation, user threads must be mapped to kernel threads. This can be done through any of the following methods:
1. Many-To-One: many user threads are mapped to a single kernel thread
    1. Very efficient
    2. System blocking calls block all threads even if they could otherwise continues
    3. Unable to be split among multiple CPUs
2. One-To-One: one user thread mapped to one kernel thread
    1. Greater overhead
    2. Can split among multiple CPUs
3. Many-To-Many: multiplexes any number of user threads to an equal or lesser number of kernel threads
    1. Combines best features of the two above
    2. Blocking kernel system calls do not block entire process
    3. Can be split among multiple CPUs