---
tags:
  - Process-Management
  - Process-Communication
---
# Message Passing
[[Process Overview | Processes]] exchange messages to cooperate. System calls and OS support are required for every message transfer. This is a slower, but simpler method in comparison to [[Shared Memory | shared memory]]. This is method also works well across multiple computers.

This is the preferred method when amount/frequency of data transfer is small or multiple computer are involved. 

## Types of Communications
Message passing can be implemented in a number of different ways, each with pros and cons.
### Direct vs. Indirect
- Direct: sender must know the name of the receiver it wishes to send a message to; creates a one-to-one link between sender-receiver pair
    - Symmetric: receiver must also know the name of the sender
    - Asymmetric: receiver does not need to know the sender's name
- Indirect: uses mailboxes or ports; multiple processes can share the same boxes; only one process can read any given message
### Synchronous vs. Asynchronous
- Synchronous: blocking communication
- Asynchronous: non-blocking communication

Both of these can be applied to either the sender or to the receiver (or to both). 
- Blocking Send: sending process is blocked until message is received ^58e0c7
- Non-Blocking Send: sending process sends the message and continues
- Blocking Receive: receiver is blocked until a message is available
- Non-Blocking Receive: receiver retrieves either a valid or null message
### Automatic vs. Explicit Buffering
These are set for when buffering is required for inter-process communication. 
- Zero Capacity: messages cannot be stored in queue
- Bounded Capacity: predetermined finite capacity in the queue; senders must block if queue if full
- Unbounded Capacity: the queue does not have predefined capacity; senders are never required to block