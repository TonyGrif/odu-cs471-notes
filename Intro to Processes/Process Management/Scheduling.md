---
tags:
  - Process-Management
---
# Scheduling
[[Process Overview| Processes]] in the [[States#^73c3f8 | ready]] state must be assigned to the processor for execution. 
## Queues
Processes [[Process Control Block | PCBs]] are kept as proxies in queues to maintain a collection of processes. The ready queue maintains a collection of ready processes. The I/O queue maintains a collection of I/O [[States#^80606b | waiting]] processes. 
## Degree of Multi-Programming
The DoM describes the number of processes that a single-processor system can efficiently accommodate. It is determined by the amount of memory allocated to [[States#^318c82 | executing]] processes, I/O needs, CPU needs, and disk speeds. 
### Equation
$\def\mp{DoM}$ $\def\rq{Ready Queue Size}$ $\def\e{Executing}$ $\def\io{IO Queue}$ $\mp=\rq + \e + \io$
## Types of Schedulers
- Short-Term: CPU schedulers, select a process from ready queue for execution on CPU
- Long-Term: Job schedulers; selects process from pool of jobs stored on disk, loads to memory, adds to ready queue
- Medium-Term: Remove process from ready queue onto disk and release its memory; the goal is to maintain a good mix of processes with different [[Burst Types| burst]] types
## Context-Switch
This occurs whenever a [[States#^318c82 | running]] process is interrupted and swapped out for another process. The swapped out process must have a [[Process Control Block | PCB]] created for swapping back in. Both the swap-in and swap-out consume the CPU's time and lead to overhead. 