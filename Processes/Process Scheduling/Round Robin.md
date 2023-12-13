---
tags:
  - Process
---
# Round Robin
Each [[Process Overview | process]] gets a small unit of CPU time every time quantum ($q$). After the quantum has elapsed, the process is preempted and added to the end of the [[Scheduling#Queues | ready queue]]. If a processes ends before the quantum does, the process is automatically released and a new process is brought in. 
## Time Quantum
This usually defaults from 10 to 100 milliseconds. When the value is high, it is similar to [[First-Come First-Served | FCFS]]. When the value is low, the [[Scheduling#Context-Switch | context switching]] overhead becomes high. 