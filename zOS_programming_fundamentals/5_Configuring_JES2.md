
# Configuring JES2

Checkpoint facility 
: Allows processes and schedules to continue after a shutdown

JES maintains snapshots of its queues or checkpoint dataset.
During JES2 initialization all jobs are stored on the spool are retained unless the operator requests a cold restart.
JES takes periodic checkpoint while printing SYSOUT data sets. 
The checkpoint data is critical to JES2 for normal processing. 

The creation of multi-access spool **MAS** complex increases the security of JES2 data and assists recovery
In MAS each system keeps its internal queue consistent with the copy in the checkpoint data set. All processors logically share the same queue. If one system crashes the other can use its checkpoint information to restart all the jobs that it was processing

`$D CKPTDEF` shows current JES2 checkpoint configuration

> both primary and secondary checkpoints are defined on DASD

NEWCKPT1 is used to specify the spare checkpoint data

> The default set name for spool data set is SYS1.HASPACE

There can be many HES nodes that communicate with each other over network 

Spool data sets must be pre-allocatd as single extent, contiguous data sets. There can up to 253 spool trakcs in JES2

Spool data sets be up to 65,535 tracks in size. If paramter `LARGED=ALLOWED` the data setsc can be 1,048,575 tracks in size

The HES22 subsystem is initialized during system startup and must be defined as a primary subsystem  because other services require the services of primary subsystem in their initialization routines

The JES2 subsystem cataloged JCL procedure is used to define the JES2 load module required by this program 

