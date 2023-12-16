---
tags:
  - Process
---
# Process Control Block
A [[Process Overview| process]] may be interrupted many times during its execution. This is a challenge as a process must continue from where it was halted. 

A process control block addresses this by storing a process' [[States | state]]. This control block acts as a data structure stored in the [[Memory Overview| memory]] of the OS containing all the necessary information to pick up where it left off.

## Contents
- The process' state
- Process Number: The PID of the process.
- Program Counter: Address of the next instruction.
- CPU Registers: Contents of the registers prior to halting.
- Memory-Limits: Info about the memory allocated to the process.
- Opened Files
- Any additional information needed to resume a process. 