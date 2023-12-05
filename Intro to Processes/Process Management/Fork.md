---
tags:
  - Processes
  - Process-Management
---
# Fork
The action of a [[Process Overview | process]] creating a "child" process. This child will be an exact replica of the parent (with a different PID). 

- Unix C Code: `fork()`
    - Returns a negative value if the creation was unsuccessful
    - Returns a zero to the newly created child
    - Returns the PID of the child to the parent
* Unix C Code: `getppid()`
    * Returns the parent's PID to the child
* Unix C Code: `getpid()`
    * Returns the PID of the process