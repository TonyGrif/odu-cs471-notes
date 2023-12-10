# Protection
## Goals
OS protection seeks to prevent malicious misuse of the system, ensure shared resources are used in accordance with system policy, ensure errant programs cause minimal damage, and enforce policies to ensure a reliable system.
## Principles
The principle of protection dictates that programs, user, and systems be given just enough to perform their tasks.
## Domain of Protection
Processes should only have access to those objects that it needs to complete its task and only in the modes for which it needs access and only during the time frame it needs access (**need to know principle**).
### Protection Domain
This specifies the resources that a processes executing in that domain may access. A domain is defined as a Venn diagram defining the domains, objects, and the the access rights.
### Domain Switching
It may be important for a process to switch domains to acquire access privileges. There must be a mechanism created for this.
### Access Matrix
This matrix represents the domains of protection. Rows represent domains and the columns represent objects. Each entry contains a set of access rights.
### Revocation
It may become pertinent to revoke access rights assigned to certain users or processes. Several questions are raised in this process
* Immediate vs. Delayed
* Selective vs. General
* Partial vs. Total
* Temporary vs. Permanent.