---
tags:
  - Virtual-Machine
---
# Virtual Machines
Virtual machines allow the host machines to emulate another computer running on it as another [[Process Overview | process]]. The host system is protected from the VM and VMs are [[Protection and Security | protected]] from each other; this means viruses are less likely to spread from one another. VMs also allow for OS research, better development efficiency, and allow for single-CPU systems to act like multiprocessor ones. 
## Hypervisor Levels
* Type 0: hardware-based solutions, support for VM creation and management through firmware.
* Type 1: OS-like software build to provide virtualization.
* Type 2: applications that run on standard OS but provide VMM features to guest OS.