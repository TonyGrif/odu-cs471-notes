---
tags:
  - Process-Scheduling
---
# Multilevel Queue
Rather than a single [[Scheduling#Queues | ready queue]] this method contains several queues for each category. Each [[Process Overview | process]] is assigned to a queue forever and each queue will have its own scheduling algorithm. The CPU will need to be shared between all the queues. 
## Multilevel Feedback Queue
This is a modified version of the multilevel queue. A process is able to move between various queues and implement aging when needed. 