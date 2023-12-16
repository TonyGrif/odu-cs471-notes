---
tags:
  - Main-Memory
---
# Segmentation
[[Memory Overview| Memory]] management scheme that supports user view of memory. In this method, each part of a program is allocated as its own entity instead of allocated the whole program as one ([[Contiguous Memory Allocation | contiguous memory allocation]]). A segmentation table is required to map segments to their [[Physical Address Space | main memory]] location. 
## Architecture
A [[Logical Address Space | logical address]] consists of two values:
1. The segment number.
2. The offset with that segment.
## Logical to Physical Mapping
The segment table is consulted to find the base and limit for the segments. The offset is checked against the limit to ensure it is valid. If it is, then $\def\base{base} \def\d{offset} \base + \d$ is used as the physical address.