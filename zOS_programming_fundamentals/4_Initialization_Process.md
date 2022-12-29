
# The Initialization Process

Initial program load
: the process by which the operating system is loaded onto the central processing complex


Hardware management console
: **HMC** used to control IBM mainframe including IPL process. T he HMC can store the IPL address, load parameter and type details in activation profiles so they do not have to be entered every time a system is initialized. Called on activate

After the IPL process has been invoked 
1. IPL 
2. Nucleus Initialization Process
3. Master Scheduler Initialization 

Although the whole process is know as the IPL, the IPL phase is the initial few microseconds when the foundation blocks of the system are laid.

> The IPL volume is accessed and it's program located, and loaded, it then receives control. IPL program is sometimes called `bootstrap`

IPL functions
1. Clearing storage
    * After storage is cleared, system searches sysres for nucleus
2. loading the nucleus
    * After loaded, IEANUc0x module loaded then passes control to the nucleus initialization program


After control form the IPL program, NIP undertakes some preliminary tasks and the perform its major function which is to process PARMLIB specified and operator specified initialization parameters

Depending on the parameter options, operator ay be prompted to enter system parameters. Can be done individually or merged content with IEASYS00

NIP Phase
* Program call / Authorization (PC/AUTH address space)
* System Trace (TRACE address space)
* Global Resource Serialization
* Dumping Service (DUMPSRV address space)
* Communication task (CONSOLE address space)

After nip has completed its work, control is handed back tot eh master scheduler initialization MSI phase

MSI Phase the initialization of the first address space is completed and the master scheduler is loaded into it. The master scheduler is processing is controlled by the JCL. 

> When MSI phase is completed you computer is ready for work 
