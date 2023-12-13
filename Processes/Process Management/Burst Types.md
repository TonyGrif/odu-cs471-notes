---
tags:
  - Process
---
# Burst Types
A [[Process Overview| process]] typically executes either CPU or I/O based instructions. Consecutive time spent on CPU-based will lead to **CPU-burst**, I/O will lead to **I/O-burst**. A **CPU-I/O burst cycle** is when one instance of each is instructed followed by the other.
## Bounding
A process that spends most of its time doing I/O operations is considered **I/O-bound**. One that spends most of its time on CPU operations is considered **CPU-bound**.  