---
tags:
  - Process
---
# Monitors
These are one of the higher-level constructs to solve the [[Producer-Consumer | producer-consumer]] problem. Monitors are classes that can only run one method at a time. Monitor methods can only access shared data within the monitor and any data passed to them as parameters. A monitor guarantees [[Producer-Consumer#Critical Section | mutual exclusion]]; however, only one [[Threads| thread]] can execute any monitor procedure at any time. It will block any thread that attempts to access if another one is already in control. This method **limits** parallelism.