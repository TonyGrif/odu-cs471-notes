---
tags:
  - Process-Management
---
# States
A [[Process Overview| process]] can enter a variety of 'states' during its lifetime. 

## List of States
- New: A new process at the start of its life.
- Ready: A process allocated memory, allowed to enter the system, and ready to execute.  ^73c3f8
- Running: Process during execution. ^318c82
- Waiting: A process waiting for the completion of an I/O or other event. ^80606b
- Terminated: Process disappearing from the system.

## Resource Allocation
Only the ready, running, and the waiting states have resources allocated to them. These are the **only** processes that matter to the operating system. 