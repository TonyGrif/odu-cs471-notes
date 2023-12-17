---
tags:
  - Storage
---
# File Systems
File systems provided efficient and convenient access to the [[Storage Overview | disk]] by allowing data to be stored, located, and retrieved easily.
## Implementation
A file system may contain info about how to boot a system stored there, the total number of blocks, the number & location of free blocks, and the [[Directories | directory]] structure and [[Files | individual files]].
## [[Directories | Directory]] Allocation
### Linear List
This uses a linear list of file names with pointers to data blocks. While being a simple method, it is also time-consuming to execute, as it utilizes linear searching to find files.
### Hash Table
Files are stored as a [[#Linear List | linear list]]; however, a hash data structure is used to take a value computed from the file name & returns a pointer to the file in the list. This decreases search time; however, as a hash table is fixed size, it becomes dependent of the hash function on that size.
## [[Files | File]] Allocation
### Contiguous Allocation
Each file occupies a set of contiguous blocks on the disk. This makes it difficult to find space for a new file and leads to [[Contiguous Memory Allocation#External Fragmentation | external fragmentation]].
### Linked Allocation
Each file is a linked list of disk blocks that can be scattered anywhere on the disk. A directory contains a pointer to the first and last block of the file and each block, itself, contains a pointer to the next block.
#### FAT
File allocation table is used at the beginning of each disk volume to speed up search times.
### Indexed Allocation
This solves the inefficient access problem by bringing all pointers into an index block. Each file has its own index block (array of disk-block addresses). The directory contains the address of the index block.
## Free Space Management
The system maintains a free-space list that records all free disk blocks.
### Bit Vector
One way the FSM is implemented. Each block is represented by one bit; if the bit is free, the bit is one; if the bit is allocated, the bit is zero.
### Linked List
One way the FSM is implemented. All free disk blocks are linked together, with the pointer to the first free block kept in a special location. Each block contains a pointer to another.