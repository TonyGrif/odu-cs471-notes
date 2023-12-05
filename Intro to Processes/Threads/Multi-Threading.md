---
tags:
  - Threads
---
# Multi-Threading
This occurs when a [[Process Overview | process]] contains multiple [[Thread Concept | threads]] that share common code, data, and certain structures specific to the program. 
## Benefits
1. Responsiveness: can utilize threads to perform quick actions and leave others to do the heavy computation
2. Resource Sharing: allows multiple tasks to be performed simultaneously in a single address space
3. Economy: creating and managing threads is faster than creating and managing processes
4. Scalability: can split among multiply processors