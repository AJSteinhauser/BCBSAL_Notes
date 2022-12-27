
#VSAM 

Virual Storage Access Method
: A type of disk set and an API for using datasets

VSAM Data sets are usually used by programs to store and manage data. They cannot be directly browsed or edited from ISPF without special software like IBM File Manager for z/OS or Computuware File-AID

VSMA features
* Speed: "Fastest data sets available for most data-related needs.
* Size: Maxiumum yield of 128 TB
* Extents: Can have up to 123 extents on each disk. Up to 255 extents

VSAM  Extended featuers
* Sharing, Data record set can be shared by multiple useres at the same time from differnt systems
* Size, a 4 gigabyte architecutual limit for data set was imposed. Max size is now 128TB
* Compression. VSAM can now be stoed in a compressed format on disk
* Speed. Improve speed using intellegent buffering and dataset striping

VSAM Users
* IMS databases
* Db2 objects
* z/Os
* CA ACF2 and RACF

5 basic types of VSAM data sets. 

## Entry Sequence Data Set
* Entry Sequenced Data Set:  **ESDS** 
    * hold fixed or variably lengthed records in any order
    * Accssed Sequentially or directly (not skip-sequentially)
    * Excellent application for logs 
    * Each record is intereted at the end of the dataset. If ther is not enough room in CI new one is started

Control Interval
: **CI** basic building block VSAM set. HOlds one or more VSAM records


Record Definition Field **RDF**
: Stores the length of each record

Control Area **CA**
: A group of CI's

## Relative Record Data Set
**RRDS**

Data is partioned into slots and data is inserted and removed from the slots.

* All records must be the same length
* Waste comes from not using the entire slot of the record
* Records cannot span slots of CIs

Advantages
* Records can be added and deleted within the data set
* Records can be directly accessed by specifying the slot number
* Skip-Sequential processing can be used 

## Linear data

* Do not hold records but just strings of data. Used by programs who specify their own data format

## KSDS 
**Key sequenced data set**

* Each data set is called a component.
* componets hold data in the same way as ESDS. 
* A part of each record is the records key
    * Key can be any 1-255 contiguous bytes in the record that are unique. Cannot be two records with the same key. Key must be the same length and position for all records
    * Key can be used to locate records
    * To change a records key, it must be deleted and re-inserted

> If there is not enough space for a new reocrd then the CI is split into two

In a CI split 1/2 of the CI is moved into a spare CI in the CA

The Index component of a KSDS holds an index into the data compnt. Oftentimes called the prime index. 

KDS data sets can accessed sequentially, directly, or skip sequentially

KSDS also allow for alternative keys such as phone numbers

## Variable-Length Relative Record Data Set
**VRRDS**
Essentially KDS that are accessed using RRN instead of key. 
Has both data component and an index component