
# Working with system parameter lists

System parameters define the way in which z/OS system is initialized

Many functions invoked during an IPL are governed by system parameters that can be tailored to the requirements of your installation.
Parameters are organized into lists, each list is stored as a member of a PDS called a parameter library or **parmlib**

Primary system parameter list is named **IEASYS00** 
* CLPA indicates the link pack area to be cleared and reloaded
* SYSNAME parameter causes the system name to be set to DEMO
* CMD specifies that the commands COMMNDD1 are to executed

The default suffix 00 us used with many parmlib members. Referred to as IEASYSxx members 
> The z/OS system provides up to 17 parmlibs in a system including the default SYS1.PARMLIB. Anyone of them could have IEASYSxx members

## Load Paramters
--------
When an operator performs an IPL of a z/OS system, a load parameter or LOADPARM will be specified it is an 8 byte string

`0100`DTP1
Bytes 0-3 used to identify the volume on which the input/output definition files resides

0100`DT`P1
Bytes 4 and 5 indicate the suffix used to form the name of theLOADxx member which is used to locate the parameter library member

0100DT`P`1 
Byte 6 is the initialization message suppression indicator **(IMSI)** which can be used to suppress certain informational messages that would normally appear on the console at UPL time
*--Oftentimes called the prompt character or feature because it determines whether the operator will be prompted for system parameter and the master catalog name.

0100DTP`1`
Byte 7 is the alternate nucleus identifier 

> The period can be used in fields where default values are desired. Spaces can also be used in fields where default values are desired but they only appear at the end of a string

This number can also be a haxadecimal. If not specified the file is assumed to be on the SYSRES volume or IPL device. Begins search on the EASYSxx number

The system searches the IODF device for a parmlib. 


NUCLEUS Parameter
: indicate the the member containing the nucleus

PARMLIB parameter
: used to create a logical pamlib concatenation. When The system uses this a s source for parmlib members during and after initialization.

SYSPARM parameter
: specify a suffix or suffixes to indicate the IEASYSxx members in the logical parmlib

Filter parameters
: so that multiple systems can use the same systems. This method is not recommended for
* it does not offer significant advantages to using individual members
* increase exposure to errors.
* Used be all systems damage it may not be possible to get any system up
* if one system is affected by an error another system can be used to repair the damage 

| Filter Name | Description |
| ----------- | ----------- |
| HWNAME | The centreal name of a processor complex |
| LPARNAME | The logical partition | 
| VMUSERID | The name of a virtual machine |

if both members contain SYSPARM parameters, all the alternate lists will be combines with IEASYS00 in the following order
1. IEASYS00
2. Members specified in LOADxx
3. Members specified in IEASYMxx