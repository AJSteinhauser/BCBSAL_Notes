# Data Security 

Existing sets are likely stored in a catalog.

Master catalog
: Main catalog. Contains entires for both data sets and sub catalogs, called user catalogs.

z/OS is also able to keep track of data sets on individual DASD volumes using Volume table of contents VTOC

### DFSMS

dfp
: Comes with z/os allows  you to create storage polices when new data is created.

dss
: optional, backups of at the data set and volume levels

hsm
: optional, moves less important or less accessed data to cheaper and slower mediums.

rmm
: optional, manage removable devices such as tape cartridges.

tvs
: optional, allows VSAM data sets to be shared between applications

Files systems supported by z/OS
* zFS
    * contains UNIX file system is a VSAM data set 
* HFS
    * Mountable file system which is being phased out by zFS
* NFS
    * Access remote unix file system using TCP/IP
* TFS
    * Temporary, in memory filesystem

Resource Access Control Facility 
: RACF provide appropriate access to the system resources (Add on)

System authorization Facility
: Default z/OS security, manages common interface for resource requests


RACF Special
: System administrator or system programmer that creates and maintains permission systems for user and data access.

> A huge threat is accidental data destruction from operators.

> All data is encrypted and only decrypted when flowing through the OS


Time sharing option (TSO)
: Initial online access to z/OS system. Large number of users to log into the mainframe environment and access data and use resources thorough DOS like interface

Mainframe access is provided through a 3270 terminal emulator connects over TCP/IP
Uses TN3270 (implementation of telnet that uses TCP/IP)

Rarely a need to use TSO commands directly, ISPF, JCL, CLISTS, and REXX programs will handle most TSO required things

> Most organizations configure their logon process to automatically continue thorough to ISPF

