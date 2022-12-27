
# Data Processing

SUBMIT
: Sends job to the system for execution

When a program executes, it informs a system about the data that is required

After a job has been submitted, JES2 or 3 will take control of the job

if JES2 separate jes2 subsystem for each processor. Each processor will handle system job i/o

if JES3, global processor will schedule all work for the other systems

All work must be schedules according to priorities and resources available. On z/os the workload management component will handle that.

POS indicate the position of the address space and may indicate why a job is not running
* IN swapped into memory indicating that is is currently running
* NS non-swap-able, commonly used for important jobs, for performance reasons are not allowed to be swapped out of memory
* LO logically swapped out of memory
* W_ indicates that it is on wait queue 

If job has been submitted but does not appear on the DA panel/ and you have not received any output, you can check SDSF input panel to check if something is delaying job execution

Some operators prefer to use SDSF status panel to display system activity

If you cannot find SDSF paensl the log enables you to view system log