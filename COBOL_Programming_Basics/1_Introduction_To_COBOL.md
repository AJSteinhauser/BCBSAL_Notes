
# Introduction to COBOL

COBOL was first proposed back in 1959
The first COBOL language was released in 1980 by a committee sponsored by US DOD called Data Systems Languages or `CODASYL`

All major computer vendors provided COBOL compilers. By the 1960's it was the most widely usd programming language in the world. 

* OOP Added in 2002
* XML in 2013

Until COBOL 85 all programming had to be done in upper case

> It is believed that there are more lines of COBOL than all other languages combined

There are many COBOL compilers today some used to support legacy systems and applications, others support modern platforms like MACOS. some compilers can produce byte code that can execute in a JVM 

COBOL 85 standard is supported by all current compilers


# Program Divisions

All COBOL programs have the same structure and is divided into 4 parts

1. Identification
2. Environment 
3. Data
4. Procedure

```COBOL
Identification Division.
Program-ID. SAMPLE.

Environment Division.
* Not used in this program.

Data Division.
* Not used in this program.

Procedure Division.
Procedure-1.
    Display 'Hello World'
    Stop Run.
```

Identification
: **Program-ID. SAMPLE.** 
The name is defined as SAMPLE

Environment
: Contains optionally provided information about where the program will run 

Data
: Working storage variables and other variables used, complex expression, constants, tables, etc.

Procedure
: Code need to process data and produce the program required output 


> The Environment and Data divisions could be omitted since they don't have useful information

```COBOL
Identification Division.
Program-ID. SAMPLE.

Procedure Division.
Procedure-1.
    Display 'Hello World'
    Stop Run.
```

Salary conversion example

```COBOL
Identification Division.       
Program-ID.  SALARY-CONVERSION.
Author.  Charlie Brown.
                
* This is a sample COBOL program.
* It will convert annual salaries to weekly salaries and
* will exit on the input of a salary of zero


Environment Division.
* Not needed in this program

Data Division.
Working-Storage Section.
01 Weeks-Per-Year  Pic 9(2)  Value 52.
01 Prompt-Message  Pic X(35) Value 'Input your annual salary: '.
01 Reply-Message   Pic X(25) Value 'Your weekly salary is: '.
```

`Program-ID and Author both end with period`

Identification options
1. Installation
2. Date-Written
3. Date-Compiled
4. Security 

`* = comments`

> Any division can be omitted if not required in the program  

**Variable naming rules**

1. (A-Z, a-z, 0-9, -, _) allowed characters
2. Does not start or end with _,-
3. Variables <= 30 characters
4. Have at least one character (Except in paragraph or sections names)
5. Not be a reserved word

> Variables are not case sensitive (COUNTER == counter == CoUnTeR)

| Variable | Description |
| -------- | ----------- |
| Zero/Zeros/Zeroes | Numeric value of 0 or regex(0+) |
| Space/Spaces | regex(\space+) |
| Quote/Quotes | ' or " |
| High-Value/High-Values | Highest character value `0xFF` or `0xFFFF`|
| Low-Value/Low-Values | lowest character value 0x0 in the character set|


COBOL was originally made of punch cards wth 80 characters on a line. Some compilers still require lines to be <= 80 chars

First 6 characters used to hold an optional value know as sequence number. Any character can be inserted here, in the past it was sequential. Not super common on modern programs, some compliers automatically insert sequence numbers

Column 7 is left blank, a asterisk means it is a comment
String literals can also use column 7 to continue the comment

Columns 8-72 contain program statements and instructions

Area A / **Margin A**
: Columns 8-11 some statements such as divisions, section headers, and variable declarations start in 8.

Area B / **Margin B**
: Columns 12-72 

Columns 73-80 usually left blank for comments or program identifier.



