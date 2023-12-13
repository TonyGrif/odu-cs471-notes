---
tags:
  - Process
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
# Process Termination
[[Process Overview | Processes]] can request their own termination or be terminated by the system.

- Unix C Code: `exit()`
    - Returns an integer value that can be passed from the [[Fork & Termination#Fork| child]] to the parent (if the parent is `wait()`)
    - Return a zero if successful completion was achieved; returns a non-zero if problems occurred
- Unix C Code: `KILL`
    - System command to end the running process
    - Usually done with the system is unable to deliver the necessary system resources
    - This command could or could not allow children to continue
        - If they are, they are referred to as **orphans**
    - Process trying to terminate but cannot because their parents are not waiting for them are called **zombies**