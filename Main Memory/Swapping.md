---
tags:
  - Main-Memory
---
# Swapping
A [[Process Overview | process]] can be temporarily swapped out of [[Main Memory Overview | main memory]] to backing store, then brought back for continued execution. This allows physical memory space of processes to exceed physical memory. Under dynamic [[Binding Instructions | binding]], the process does not need to go back to the same part of memory. The [[Scheduling#Context-Switch | context-switch time]] could become very high.