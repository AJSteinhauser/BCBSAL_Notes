
# Program Control

Procedure divisions consists of statements grouped into sentences

```COBOL
Main-Program Section.
Paragraph-1.
Move 1 to WS-A
Move 45 to WS-B.

End-Program Section.
    Stop Run.
```

Section. 
: Marks the beginning and end of a section, *see above example*


```COBOL
Main-Program Section.
Paragraph-1.
Move 1 to WS-A
Move 45 to WS-B.

Paragraph-2.
    Stop Run.
```

Paragraph
: Paragraph ends when a new section or section is declared, *see above example*

Perform
: Is like a list of functions to call

Exit Paragraph
: A paragraph at the end of a group of sentences containing only an Exit statement

Go To Statement
: Pass control to a section or paragraph, control is not returned back unlike perform

Stop
: A command halt the execution of a program and display message to COBOL operator 

> Stop Run should be the last statement to be executed in COBOL program

Options for if statements

* AND 
* OR
* NOT
* \> 
* GREATER
* LESS 
* = 
* EQUAL

If statements can be closed two ways
* Period
* `End-If` Statement

Evaluate Statement
: Similar to switch statement in other languages

```COBOL
Evaluate Employee-Type
    When "A" Move 25.00 To Normal-Rate
    When "B" Move 29.00 To Normal-Rate
    When Other Perform Report-Error
End-Evaluate.

```

Thru
: Range of options to test condition against

Perform _Procedure_Name_ (int) times
: Able to run procedure multiple times
```COBOL
Perform Procedure-x 10 Times
```

Perform _Procedure_Name_ Until Statement
: While loop for COBOL

```COBOL
Perform Procedure-x Until Counter = 10
```

**For Loop COBOL edition**
```COBOL
Perform Procedure-x
    Varying Total-Counter From 1 by 1 
    Until Total-Counter > 10
```

**Inline loop**
```COBOL
Perform 10 Times
    ...
    ...
End-Perform.
```

**Inline conditional loop**
```COBOL
Perform With Test Before Until Employee-Name = Spaces
   statement
   statement
End-Perform.
```
*With Test Before Until is implied by compiler*

```COBOL
Perform Until Employee-Name = Spaces
   statement
   statement
End-Perform.
```

**Do While Loop**
Checks condition after loop runs at least once
```COBOL
Perform With Test After Until Employee-Name = Spaces
   statement
   statement
End-Perform.
```
