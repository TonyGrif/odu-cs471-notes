---
tags:
  - Process
---
# Shared Memory
[[Process Overview | Processes]] cooperate by sharing common [[Memory Overview| memory]]. This memory is allocated in the address space of one process that can then be accessed by other processes. No system calls are required and, as such, it is a faster method is comparison to [[Message Passing | message passing]]. However, it is much more complicated to set up and does not work well across [[Distributed Systems | multiple computers]]. 

This method is preferred when large amounts/quantity of information must be shared quickly on the same computer. 

This method is commonly used in [[Producer-Consumer | producer-consumer]] problems.