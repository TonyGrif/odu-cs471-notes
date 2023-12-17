---
tags:
  - Main-Memory
---
# Memory Overview
For a [[Process Overview | process]] to run, it must first be brought from the [[Storage Overview | disk]] and placed into main memory. Main memory is responsible for storing programs and data that the processor is actively using. Instructions must be **bound** to main memory before usage. This can occur at compile, load, or run time.
## Base and Limit Registers
A base and limit define the bounds of a logical address space. The **base** specifies the starting point, while the **limit** defines the length of the space. Every memory access generated in user mode is checked by the CPU to ensure it is operating in proper memory. If outsides these bounds, a **fatal error** is flagged.
## Memory Type
* [[Logical Address Space]]
* [[Physical Address Space]]
* [[Memory-Management Unit]]
## Physical Memory
* [[Swapping]]
* [[Contiguous Memory Allocation]]
## Virtual Memory
* [[Logical Address Space]]
## Paging
* [[Paging]]