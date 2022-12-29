
# Virtual storage and address space 


Virtual storage is the paging method of swapping memory in and out of frames

System resource manager (SRM) can go around the overhead of swapping address space by logical swapping. Keeps the address in real storage but makes it look like it has been swapped out

When the task completes real and auxillary storage is released for use by other tasks

Programs virtual storages is divided into pages. Each page is fixed size 4KB. Db2 can use larger 1MB sized pages 

| Storage type | Container name | Size |
| ------------ | -------------- | ---- |
| Real Storage | Frames | 4kb or 1 mb|
| Auxillary  | Slots | 4KB or 1 mb|
| Virtual Storage | Pages | 4KB or 1 mb|

> With virtual storage you can have relatively small amount of real storage support a large number of tasks

> The system provides each user or program with their own address space which is capable of providing virtual address's available for executing instructions and storing data.

Each address space id divided into two types of storage: Common and private

Common Storage
: Contains modules that common to many users. Prevents duplication and minimizes waste

Private Storage
: Contain data that is unique to each individual address space

With z/OS 64 bit addressing was introduced and gives programs 16 EB of virtual storage, an increase of 8 billion times more than previous versions

