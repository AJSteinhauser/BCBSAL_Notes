# Move Data

> In COBOL data is defined by the Picture facility

Conventions for Data Transfer
* All currency items should have a common picture PIC S9(8)V9(2)
* All counters should have a common picture 

Memory allocations of the past limited variable sizes. Now it is better to be generous than to lose data

It is good practice to store money in the smallest currency unit. Can be converted to other version later

Move Statement
: Copies the contents of the source item to the destination. 

Two types of move
* Numeric 
* Alphanumeric

Initialize
: Set value of variable 

```COBOL
Data Division.
01 Customer-Balance Pic s9(8)v9(2) Value 4356.75
01 Customer-Balance-Display Pic $zz,zz9.99.

Procedure Division.
    Move Customer-Balance to Customer-Balance-Display
    Display "Customer Balance :" Customer-Balance-Display
```

`Pic $zz,zz9.99.`
`$` number should proceeded by $
`z` indicates a digit or a space if digit is 0
`.` indicates that period should be inserted


| Editing Character | Result |
| --------------| --------- |
| B | Insert Space |
| / | Insert / |
| Z | Leading characters will be replaced with a space|
| . | Insert decimal point . |
| , | Insert Comma | 
| * | Replace leading 0's with * |
| - | Add minus sign at beginning if data is negative |
| + | add minus sign at beginning if data is negative and add + is data is positive |
| $ |  Insert currency symbol at front |
| CR | Characters CR added to end if numeric data is positive |
| DB | Characters DB added to end if numeric data is negative |


