---
tags:
  - Main-Memory
---
# Contiguous Memory Allocation
[[Main Memory Overview | Memory]] is allocated contiguously and the only information needed is the starting address or the base address & its size.
## Partitioning
Resident operating system is usually held in low memory with an interrupt vector. User processes are held in high memory.
### Multiple Partition
This strategy utilizes partitions where one process is exclusive to. These can be fixed-size or variable. This method leads to a great deal of holes.
#### Dynamic Storage Allocation
Utilizing variable-size partitions, there exist methods to determine which free partition to allocate to:
1. First-fit: first hole big enough starting from top of memory
2. Best-fit: the smallest hole that is big enough
3. Worst-fit: the largest hole that is big enough
## Fragmentation
A phenomenon where storage space is used inefficiently though wasted space.
### External Fragmentation
The total memory exists for a request, but it is not contiguous. 
#### Solutions
1. Compaction: moving all allocated memory blocks into a single unit by combining all free memory holes
2. Garbage Collection: collects all inaccessible memory and returns them as free
3. [[Paging]]
### Internal Fragmentation
The amount of memory allocated to a process is greater than requested.