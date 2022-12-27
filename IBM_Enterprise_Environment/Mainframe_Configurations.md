
# Mainframe configurations

z/VM
: Virtual machine is an OS that enables organizations to run multiple operating systems on a single machine.

Hypervisor
: z/VM acting as a stand along OS

Latest version of z/VM are designed to enable clients to run thousands of linux images on a single IBM Z mainframe

In recent years the KVM hypervisor has been added to provide orgs. with alternate open-source virtualization solutions

z/VSE OS is commonly used with smaller mainframes. 

Linux mainframe is know as Linux on IBM Z

Some orgs reported performance increases from being able to split applications so they  run on their own linux instance

z/TPF
: Transaction processing facility. Suited for high transaction volumes. Utilize multiple mainframes to handle tens of thousands of transactions

z/OS 
: Premier 

In mainframes storage means
* Area where the program resides in order for them to run
* The medium used to store data

Auxillary storage
: External to the mainframe. Paging storage

Channel Subsystem
: External communication to send data to devices

Sysplex
: Allows shared resources between multiple mainframe devices

LPAR
: Logical partitions, separates divisions for testing, development, and production environments z/OX 2.3 on z14 supports up to 4TB of memory per LPAR

z/OS communication server components
1. SNA protocol stack which is apart of virtual telecommunications access method (VTAM)
2. TCP/IP protocol stack 
3. Communications storage manager (CSM) provides shared I/O data flow 


SNA
: Original networking architecture that allowed mainframes to communicate with each other.

Today TCP/IP is the most common way to communicate over a network

OSA
: Open system adapter, network controller that allows the mainframe to communicate with a number of LANS over SNA and TCP/IP through a operation called queued direct I/O **QDIO**


