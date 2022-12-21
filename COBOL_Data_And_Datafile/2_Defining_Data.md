
# Data Division

4 Sections of the Data Division
* File Section
* Working-Storage Section
* Linkage Section
* Report Section


3 Spicy sections supported by some compilers
* Local-Storage Section
    * Essentially a call stack frame for local dat
* Screen Section
    * Defines format and content of non-scrolling-full-page screens
* Communication Section
    * Defines the structure of information sent or received with communication devices  


File-Section
: Defines format and structure of all input and output files the program will process

Working Section
: Defines structure and format of all data areas used in a program.

Linkage Section
: Defines the format of parameter passed ot this program by calling a program

Report Section
: Defines the format and contents of one or more reports fo ruse with the COBOL report writer.

# Format 

All single elements have a level of 01

```COBOL
01 Employee-Counter Pic 9(4).
```

Codes for picture structures
* 9 Positive Numeric
* S9 Integer
* A Alphabetic character
* X Alphanumeric character
* V to designate number of decimal places
* N Unicode or national character

```COBOL
01 Employee-Counter Pic 9(3)V9(2).
* 153.45 stored as 15445 and displayed the same
```

Value Declarations are used to "Preset" the value of a variable
```COBOL
01    Employee-Counter    Pic 9(4) Value 15.
01    Employee-Name       Pic X(30) Value Spaces.
01    Tax-Payable         Pic 9(2)V9(2) Value 9.50.
01    Error-Message       Pic X(50) Value "An error was encountered.".
```

