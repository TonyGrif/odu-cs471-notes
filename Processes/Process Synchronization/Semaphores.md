---
tags:
  - Process
---
# Semaphores
These are one of the higher-level constructs to solve the [[Producer-Consumer | producer-consumer]] problem. A semaphore is an integer variable that can be accessed only through atomic `wait` and `signal` instructions.
## Wait Instruction
The wait function will decrement the integer value; then, it will block the [[Threads| thread]] until the value is greater than zero.
## Signal Instruction
The signal function will increment the integer value; then, it allow another [[Threads| thread]] to enter.
## Types
There are two types of Semaphores.
### Binary (Mutex) Semaphore
This represents a single access to a resource, meaning only one [[Threads| thread]] can access it at a time. This guarantees [[Producer-Consumer#Critical Section | mutual exclusion]].
### Counting Semaphore
This represents a resource with many units available. Multiple [[Threads| threads]] can pass the semaphore at a time and is determined by the semaphore count.
## Pseudocode
```
Semaphore sem;
do {
    wait(sem);
    /* Critical Section */
    signal(sem);
} while (True);
```