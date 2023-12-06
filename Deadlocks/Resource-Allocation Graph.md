---
tags:
  - Deadlock
---
# Resource-Allocation Graph
This is a directed graph to represent processes and the resources that possess and request. It consists of vertices and edges. It can be used to detect [[Deadlock Overview | deadlocks]].
## Vertices
These are the processes and the resources in the system.
$P = {P_1, P_2, ..., P_n}$, these are indicated by circles.
$R = R_1, R_2, ..., R_n$, these are indicated by squares.
## Edges
These are the allocation and request links.
* Request Edge: $P_i -> R_j$, process $P_i$ requests $R_i$.
* Assignment Edge: $R_j -> P_i$, resource $R_j$ is allocated to $P_i$.
## Determining Deadlock
* If a graph contains no cycles, there are **no** deadlocks.
* If a graph contains a cycle:
    * If each resource involved only has one instance, there **is** a deadlock.
    * If several instances of a resource involved exists, there **may** be a deadlock.