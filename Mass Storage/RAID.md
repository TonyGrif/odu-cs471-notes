---
tags:
  - Mass-Storage
---
# RAID
RAID seeks to offer improvements in reliability through redundancy. This ensure that if one disk fails, there is a way to get the data back and none is lost.
## Level 1
Each disk contains an identical image on another disk.
## Level 2
This method employs error-correcting code by utilizing parity bits. This allows a damaged disk to be recreated from the data disks and other parity disks.
## Level 3
This utilizes bit-interleaved parity and a single parity bit disk. This allows a single parity bit to be used for error detection and correction. This reduces the storage overhead; however, it supports less I/O per second.
## Level 4
This utilizes block-interleaved parity. It uses block-level stripping and keeps a parity block on a separate disk for corresponding blocks for the other disks.
## Level 5
This utilizes block-interleaved distributed parity. It spreads the data and parity among $N+1$ disks. This is the most common RAID system.
## Level 6
This method stores extra redundant information to guard against multiple disk failures. This uses error-correcting codes instead of parity.