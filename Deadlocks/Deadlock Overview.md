---
tags:
  - Deadlock
---
# Deadlock Overview
Several [[Process Overview | processes]] may compete for a finite number of resources; if a resource is unavailable, the process enters the [[States#^80606b | waiting state]]. If the resource is held by another  process waiting for a different resource, the program enters a deadlock.
## Deadlock Conditions
Deadlock occurs if all four of the following conditions hold simultaneously:
1. Mutual Exclusion: only one process can use a resource
2. Hold & Wait: a process holding at least one resource is waiting to acquire additional resources held by others
3. No Preemption: resource can be released only voluntarily by a process after the task is completed
4. Circular Wait: there exists a set of waiting processes such that $p_0$ is waiting for a resource held by $p_1$, $p_1$ is waiting on a resource from $p_2$, ..., $p_{n-1}$ waiting on $p_n$, and $p_n$ waiting on $p_1$
## Notation
Resources are denoted as $r_n$ and each resource type may have one or more instances.