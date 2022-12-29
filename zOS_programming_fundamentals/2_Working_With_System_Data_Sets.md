# Working with system data sets 

SYS1.NUCLEUS
: Contains the nucleus and is cered during system build. During system initialization, members of it are bought into central storage to initial other z/os components. *ALWAYS RESIDES IN SYSRES VOLUME*

Hardware configuration definition
: **HCD** Provides user with simple interface to enter system hardware and software configuration. produces an I/O definition file **IODF** modern day version of this are GUI based. 

System  programmer can specify the IODF data set to be used when initializing the system. Is a member of the SYSn.IPLPARM or SYS1.PARMLIB data set called LOADxx

xx part of LOADxx are two character chosen by the system programmer. 

SYS1.PARMLIB
: Partitioned data set whose memebers contain a list of system parameter values that set limits or controls the behavior of z/OS. Can be grouped as PARMLIB the LOADxx member and IEASYSnn members supplies parameter and pointers that are used during IPL
*--Can be named anything these days*

LOADxx also contains a pointer to the master catalog. Thi sis the link to the location of most of that data sets

During IPL the master catalog is used to locate system data sets that are not ont eh SYSRES volume

SYS1.LPALIB
: Contains read-only system supplied executable programs or routines which are loaded in the pageable link pack area **PLPA** 
*--Can be named anything these days*

SYS1.PROCLIB
: Contains JCL procedures that used for subsystem, started tasks including JES2, TSO, LLA, and VTAM. 
*--Can be named anything these days*

SYS1.LINKLIB
: group of datasets containing operating system related executable programs and routines, as well as programs written by users for general use
*--Can be named anything these days*

Load Libraries
: Contain all the executable programs that have been compiled and bound - link-edited and are ready to run **LOAD, LOADLIB, LINKLIB will usually be in their names**

Page Data Sets
: Consitute the auxillary storage that is used to hold invidual pages of virtual storage when they are paged out of real storage. 
*--IIEASYS00 or IEASYSxx contain page set definitions*

JES
: Handles batch jobs that are submitted for execution by using spool data sets for input and output processes. Before JES is fully initialized, however spool data sets must be created. 

SPOOLDEF
: Initialization statement which is located in a JES2 to modify attributes such as buffer sizes, actual spool data set naems SYS1HASPACE and volumes the data sets are going to be placed on.

> SYS1 qualifiers are used to maintain the OS

System modifications are distributed by IBM and implementation is managed by System Modification Program/Extended **SMP/E** 


**SMP/E functions**
* Enables selection of changes to be installed
* Invokes utility programs that will implement the selected changes
* Performs a change management task and records details about the implementation


