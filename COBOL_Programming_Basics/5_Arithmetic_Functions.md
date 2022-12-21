

# Arithmetic Operations

### ADD

* `Add <Item-1> [Item 2] ... to [Item-n]`
* `Add <Item-1> [Item 2] ... giving [Item-n]`

> Ensure output result can fit into correctly sized data point

### Subtract

* `Subtract <Item-1> [Item 2] ... from [Item-n]`
* `Subtract <Item-1> [Item 2] ... from [Item-n] giving Item-x`

> COBOL will not automatically cater for negative results. If the data is able to hold negative results then must have a signed picture definition.

```COBOL
Account-balance Pic S9(8)V9(2).
* Signed example
```

### Multiply 

* `Multiple Item-1 by Item-2`
* `Multiple Item-1 by Item-2 giving Item-3`

### Dividing 

Different diving methods
```COBOL
Divide Item-1 into Item-2
Divide Item-1 by Item-2 Giving Item-3
Divide Item-1 into Item-2 Giving Item-3
Divide Item-1 by Item-2 Giving Item-3 Remainder Item-4
Divide Item-1 into Item-2 Giving Item-3 Remainder Item-4
```

On Size Error
: Conditional logic when not enough space was allocated for the data


Compute Statement
: Lets you plug in an equation more similar to modern languages

```COBOL
Compute Total-Wage = Hours-Worked * Hourly-Rate + Bonus

Compute Square-Root Rounded = Number-X ** 0.5

Compute Tax-Payable = (Wage-Bonus+Allowance)*Tax-Rate/100
    On Size Error Display "Client is over-taxed"
End-Compute

Compute Actual-Price = Quoted-Price*(1-Discount-Rate/100)
```

*\*\* Is used to denote exponentials*

