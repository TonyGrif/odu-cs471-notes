---
tags:
  - Security
---
# Protection
The OS **goals** of protection seeks to prevent malicious misuse of the system, ensure shared resources are used in accordance with system policy, ensure errant programs cause minimal damage, and enforce policies to ensure a reliable system. The **principle** of protection dictates that programs, user, and systems be given just enough to perform their tasks.
## Domain of Protection
[[Process Overview | Processes]] should only have access to those objects that it needs to complete its task and only in the modes for which it needs access and only during the time frame it needs access (**need to know principle**).
### Protection Domain
This specifies the resources that a processes executing in that domain may access. A domain is defined as a Venn diagram defining the domains, objects, and the the access rights.
### Domain Switching
It may be important for a process to switch domains to acquire access privileges. There must be a mechanism created for this.
### Access Matrix
This matrix represents the domains of protection. Rows represent domains and the columns represent objects. Each entry contains a set of access rights.
### Revocation
It may become pertinent to revoke access rights assigned to certain users or processes. Several questions are raised in this process:
* Immediate vs. Delayed?
* Selective vs. General?
* Partial vs. Total?
* Temporary vs. Permanent?
# Security
OS security deals with protecting systems from deliberate attacks from either internal or external agents.
## Common Violations
* Bread of Confidentiality.
* Breach of Integrity.
* Breach of Availability.
* Theft of Service.
* Denial of Service.
## Levels of Security
* Physical.
* Human.
* Operating System.
* Network.
# Cryptography
This method of [[#Security | security]] ensures secure communication over insecure medium. The idea is to encode a message so that the receiver is the only entity that can decode and read it.
## Symmetric
Symmetric cryptography uses the same key for the encryption and decryption.
## Asymmetric
Asymmetric cryptography uses a different key for encryption and decoding. It is important to note that the keys cannot be derived from each other; this allows the encryption key to be made publicly available.
### Digital-Signature Algorithm
This produces authentication (digital signatures) that are used for the receiver to verify that the message came from a trusted source and has not been modified in transit.