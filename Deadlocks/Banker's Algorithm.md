---
tags:
  - Deadlock
---
# Banker's Algorithm
This is one way to avoid [[Deadlock Overview | deadlocks]] in a system where resources have multiple instances. This is done by ensuring the system remains in a [[Safe State | safe state]].
## Definitions
* $N$ is the number of processes.
* $M$ is the number of resources.
* Available is a vector of length $M$ indicating the number of available resources of each type.
* Max is a $NxM$ matrix defining the max demand of each process.
* Allocation is a $NxM$ matrix defining the number of resources of each type are allocated to each process.
* Need is a $NxM$ matrix indicating the remaining resources needed by a process.