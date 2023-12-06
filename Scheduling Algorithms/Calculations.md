---
tags:
  - Process-Scheduling
---
# Calculations
[[Scheduling#Types of Schedulers| Schedulers]] are responsible for scheduling [[Process Overview | processes]] to the CPU. Calculating their efficiency refers to the following metrics: 
* CPU Utilization: how long the CPU is busy
    * $\def\tbt{total burst time} \def\tet{total elapsed time} \dfrac{\tbt}{\tet}$
* Throughput: number of processes that complete their execution per time unit
    * $\def\tbt{totalBurstTime} \def\tnp{totalNumberProcesses} \dfrac{\tbt}{\tnp}$
* Turnaround Time: time between a process entering to the time it terminates
* Waiting Time: time a process waits in the [[Scheduling#Queues | ready queue]]
* Response Time: time a process waits for a first time accessing the CPU
## Objectives
Scheduling algorithms attempt to achieve one or more of the following:
* Maximum CPU Utilization
* Maximum Throughput
* Minimum Turnaround Time
* Minimum Waiting Time
* Minimum Response Time