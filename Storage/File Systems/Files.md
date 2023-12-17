---
tags:
  - Storage
---
# Files
A file is a single, logical, and nonvolatile [[Storage Overview | storage]] unit mapped by the OS to physical devices.
## Attributes
* Name: symbolic name kept in human readable form.
* Identifier: unique tag identifying the file within the system.
* Type.
* Location.
* Size.
* Protection: access-control information determining who can read, write, execute, etc.
* Time, Date, User Identification.
## Access Methods
There are two methods for accessing a file.
### Sequential Access
This is the simplest and most common method. Information is processed in sequential order.
### Direct (Relative) Access
Files are made up of fixed-length logical records that allow the program to read & write rapidly in no order.