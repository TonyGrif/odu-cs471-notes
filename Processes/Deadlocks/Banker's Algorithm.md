---
tags:
  - Process
---
# Banker's Algorithm
This is one way to avoid [[Deadlock Overview | deadlocks]] in a system where resources have multiple instances. This is done by ensuring the system remains in a safe state.
## Safe State
A system is in a safe state if there exists a sequence of all [[Process Overview | processes]] in the system that can safely request, allocation, and finish without a deadlock occurring.
## Definitions
* $N$ is the number of processes.
* $M$ is the number of resources.
* Available is a vector of length $M$ indicating the number of available resources of each type.
* Max defines the max demand of each process.
* Allocation defines the number of resources of each type are allocated to each process.
* Need indicates the remaining resources needed by a process.
## Example Matrix
$$
\begin{bmatrix}
 & Allocation & Max & Available & Need\\
 & r_0, r_1, ..., r_n & ... & ... & r_0, r_1, ..., r_n \\
p_0 & int_0, int_1, ..., int_n & ... & ... & int_0, int_1, ..., int_n \\
p_1 & \\ 
... & \\
p_m
\end{bmatrix}
$$