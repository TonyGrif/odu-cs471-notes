---
tags:
  - Process
---
# Client-Server Communication
In client-server systems, clients send requests to the server and the server typically sends back a reply. These systems must utilize [[Message Passing | message passing]] to handle [[Inter-Process Communication | inter-process communication]]. 
## Strategies
There are a number of strategies to implement this communication, each with their own pros and cons.
### Sockets
A socket is an endpoint for communication defined by the concatenation of an IP address and a port number.
### Remote Procedure Calls
Procedure calls are similar to calling on the local machine, except the procedure is on a remote machine. This requires the use of stubs on either end of the connection. A common example of this is a [[Storage Access#Network-Attached | networked file system]].
#### Steps
1. Local process calls on the stub.
2. RPC system marshals the parameters to the procedure call and transmits to the remote system.
3. Remote machine's RPC daemon accepts the parameters and calls upon the appropriate remote procedure.
4. Results are packaged up and set to the local system's RPC system which then unpackages and returns the results to the local procedure.
### Pipes
Pipes are simple channels of communication between processes.
#### Considerations
1. Is this unidirectional or bidirectional communication?
2. Is bidirectional half or full duplex?
3. Must a relationship, such as parent-child, exist between processes?
4. Can pipes communicate over a network or just locally?
#### Two Types of Pipes
* Ordinary Pipes: unidirectional pipes with a reading and a writing end.
* Names Pipes: pipes that exist beyond the lifetimes of certain processes; support bidirectional communication and communication between related processes.