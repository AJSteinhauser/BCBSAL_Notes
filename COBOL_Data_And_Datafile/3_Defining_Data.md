
# Display Data

X and N are padded to right with spaces

By default COBOL 

`Usage Display` tells COBOL to save the number as ASCII string


Store data as efficiently as possible
* `Usage is Computational`
* `Usage Comp`
* `Comp` 

Also Comp-4 is another way of instructing COBOL to store number as binary
* `Usage is Computational-4`
* `Usage Comp-4`
* `Comp-4` 

Negative numbers are stored as Two's complement binary numbers

`Packed-Decimal` is another method where ach decimal digit is stored as 1/2 of a byte. C or F = positive. 

Floating point options
* `Float` 
* `Float-Short`
* `Comp-1`
* `Comp-2`
* `Double`

In computational variables can be shared with other programming languages such as C or PL/I. Display variables cannot

> Filler can be assigned to data which is not required to have a specific name of its own.

All level one data items must be unique

Qualifiers are used as accessors to data

* Display Emp-Number of Employee-Old.
* Display Street in Emp-Address of Employee-New.
* Display Street in Employee-New.
* Display Hourly-Rate of Employee-New.

