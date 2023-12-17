---
tags:
  - Main-Memory
---
# Dynamic Relocation
By utilizing a relocation register, a routine does not need to be loaded to [[Memory Overview| memory]] unit it is called. This leads to better memory-space utilization by keeping unneeded information on [[Storage Overview | disk]].
# Dynamic Linking
This postpones linking libraries and program code together until execution time. A small piece of code (stub) is used to locate the appropriate memory-resident library routine; then, it replaces itself with the address of the routine.