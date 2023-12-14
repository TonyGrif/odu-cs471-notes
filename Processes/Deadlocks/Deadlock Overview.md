---
tags:
  - Process
---
# Deadlock Overview
Several [[Process Overview | processes]] may compete for a finite number of resources; if a resource is unavailable, the process enters the [[States#^80606b | waiting state]]. If the resource is held by another  process waiting for a different resource, the program enters a deadlock.
## Deadlock Conditions
Deadlock occurs if all four of the following conditions hold simultaneously:
1. Mutual Exclusion: only one process can use a resource.
2. Hold & Wait: a process holding at least one resource is waiting to acquire additional resources held by others.
3. No Preemption: resource can be released only voluntarily by a process after the task is completed.
4. Circular Wait: there exists a set of waiting processes such that $p_0$ is waiting for a resource held by $p_1$, $p_1$ is waiting on a resource from $p_2$, ..., $p_{n-1}$ waiting on $p_n$, and $p_n$ waiting on $p_1$.
## Deadlock Detection
Deadlocks can be detected through the use of either [[Resource-Allocation Graph | resource-allocation graphs]] or [[Banker's Algorithm | Banker's algorithms]]. Resource-allocation graphs are best used for instances of a single resource; Banker's algorithm is best used for instances of a resource with multiple instances.
## Deadlock Breaking
Deadlocks can be broken by aborting one or more [[Process Overview | processes]] causing the [[Deadlock Overview#Deadlock Conditions | circular wait]] or by preempting some resources from one process to a deadlocked one. Most operating systems will not attempt to break a deadlock and, instead, leave it to the user and application developers.
### Aborting
This method breaks the cycle by aborting a deadlocked process. All partial computations are lost and may have to be recomputed later. One process is aborted at a time until the deadlock is cleared.
### Preemption of Resources
This method will temporarily take some resources from one or more processes and give it to the deadlocked one to proceed.
#### Victim Election
Preemption must have an algorithm for selecting a process to take resources from. This must factor in the number of resources the process is holding and the amount of time it has consumed thus far.
#### Rollback
A plan must be in place for what to do with the preempted process. The process must rollback to a safe state and continue from there. The simplest solution is to [[#Aborting | abort]] the process and restart it. If not, this will require the system to keep track of more information about the previous states of all running processes.
#### Starvation
It must be determined if the same process can be preempted multiple times.