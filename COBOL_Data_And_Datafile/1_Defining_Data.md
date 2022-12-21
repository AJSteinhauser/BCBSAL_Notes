
# Conventions

`The convention is Pascal-Case-With-Hyphens`

Variables are defined in the Data Division

Similar to ASM code it is cleaner and good practice to define constants and other variables in the Data Division

Rules for writing COBOL syntax
* Avoid reserved words
* Follow conventions
* Numeric literals and figurative constants must be written correctly
* Properly define data items
* Where possible, variables should be used instead of inline literals


COBOL accepts two data types. Numeric and Alphanumeric. Numbers include binary, integers, floating point, ext...

* Text is stored as a string of characters 
* Computational is stored efficiently in binary format. Allowing for quick arithmetic operations to be performed.
* Display is stored as a number ready for display

Data stored in COBOL can be single or a group of elements. Elementary variables are normally sorted as single items. Group variables consist of one or more variables `Struct`

| Storing Type | Description |
| -------------| -------------|
| Text | Treated as string, no arithmetic possible |
| Computational | Efficiently stored for arithmetic, does not display well| 
| Display | Stored as a number formatted for display, no arithmetic possible |