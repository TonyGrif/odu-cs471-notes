---
tags:
  - Main-Memory
---
# Main Memory
For a [[Process Overview | process]] to run, it must first be brought from the disk and placed into main memory.
## Base and Limit Registers
A base and limit define the bounds of a logical address space. The **base** specifies the starting point, while the **limit** defines the length of the space. Every memory access generated in user mode is checked by the CPU to ensure it is operating in proper memory. If outsides these bounds, a **fatal error** is flagged.