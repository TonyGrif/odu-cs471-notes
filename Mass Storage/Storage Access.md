# Storage Access
Computer can access disk storage through either I/O ports or through network-attached storage.
## Host-Attached
This method is accessed through I/O ports through either IDE, ATA, or SATA technologies.
## Network-Attached
This method has the storage system accessed remotely over a data network. Clients access this storage through remote-procedures (NFS for UNIX, CIFS for Windows). The [[Client-Server Communication#Remote Procedure Calls | remote procedure calls]] are carried via TCP or UDP over an IP network.
## SAN
Storage-area network is a private network connecting servers and storage units. A SAN switch can allow or prohibit access between host and storage. 