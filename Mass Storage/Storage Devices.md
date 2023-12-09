# Magnetic Disks
Magnetic disks contain multiple disk platters that store information by recording it magnetically. A read-write head moves above each platter for data access. Each platter is logically divided into circular tracks that are subdivided into sectors.
## Random-Access Time
This is the time to move the disk head to the correct position and is determined by:
1. Seek Time: time to move disk arm to cylinder
2. Rotational Latency: time for t;he desired sector to rotate under the disk head
## Scheduling
Scheduling methods must be implemented to determine where the read-write head should move next.
### FCFS
First request gets served first.
### SSTF
This selects the request with the shortest seek time from the current head position.
### SCAN
The disk arm starts at one end of the disk and moves to the other end, servicing requests as it goes.
### C-SCAN
Similar to [[#SCAN | SCAN]], this algorithms starts at one end and goes to the other. The difference is C-SCAN does not service on the return and just goes back to the front.
### LOOK
This method is similar to [[#SCAN | SCAN]]; however, it does not move the full width of the disk. Instead, the arm only goes as far as the furthest request in either direction.
# Solid State Disk
An SSD is a nonvolatile storage device. They have the same characteristics of [[#Magnetic Disks | magnetic disks]] but are more reliable and faster.