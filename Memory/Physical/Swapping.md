---
tags:
  - Main-Memory
---
# Swapping
A [[Process Overview | process]] can be temporarily swapped out of [[Memory Overview| main memory]] to backing store, then brought back for continued execution. This allows physical memory space of processes to exceed [[Physical Address Space | physical memory]]. Under dynamic binding, the process does not need to go back to the same part of memory. The [[Scheduling#Context-Switch | context-switch time]] could become very high if done often enough.