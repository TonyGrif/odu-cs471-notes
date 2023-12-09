---
tags:
  - Main-Memory
---
# Segmentation
[[Main Memory Overview | Memory]] management scheme that supports user view of memory. 
## Architecture
A [[Logical Address Space | logical address]] consists of two values:
1. The segment number
2. The offset with that segment
## Logical to Physical Mapping
The segment table is consulted to find the base and limit for the segments. The offset is checked against the limit to ensure it is valid. If it is, then $\def\base{base} \def\d{offset} \base + \d$ is used as the physical address.