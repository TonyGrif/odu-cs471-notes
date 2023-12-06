---
tags:
  - Deadlock
---
# Deadlock Breaking
[[Deadlock Overview | Deadlocks]] can be broken by aborting one or more [[Process Overview | processes]] causing the [[Deadlock Overview#Deadlock Conditions | circular wait]] or by preempting some resources from one process to a deadlocked one.
## Aborting
This method breaks the cycle by aborting a deadlocked process. All partial computations are lost and may have to be recomputed later. One process is aborted at a time until the deadlock is cleared.
## Preemption of Resources
This method will temporarily take some resources from one or more processes and give it to the deadlocked one to proceed.
### Victim Election
Preemption must have an algorithm for selecting a process to take resources from. This must factor in the number of resources the process is holding and the amount of time it has consumed thus far.
### Rollback
A plan must be in place for what to do with the preempted process. The process must rollback to a safe state and continue from there. The simplest solution is to [[#Aborting | abort]] the process and restart it. If not, this will require the system to keep track of more information about the previous states of all running processes.
### Starvation
It must be determined if the same process can be preempted multiple times.