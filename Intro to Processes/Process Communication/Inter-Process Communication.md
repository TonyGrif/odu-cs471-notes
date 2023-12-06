---
tags:
  - Process-Communication
---
# Inter-Process Communication
[[Process Overview | Processes]] can be either independent or cooperating. Processes that cooperate are able to affect and be affected by other processes. These process can communicate either through [[Message Passing | message passing]] or [[Shared Memory | shared memory]]. 
## Benefits to Cooperation
- Information Sharing: using the same file
- Computation Speedup: break down a large tasks to sub-tasks to be solved simultaneously
- Modularity: break down application into cooperating modules where each module is a process
- Convenience: multi-tasking