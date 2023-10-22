# Type Inference Implementation

This project involves the implementation of a type inference program in OCaml. The program is designed to analyze terms from the Simply Typed Lambda Calculus and determine their types. The README provides an overview of the code structure and functionality.


## Code Structure

### Syntax
```
NUMBER ::= DIGIT | NON_ZERO_DIGIT DIGIT_SEQ
DIGIT ::= 0 | NON_ZERO_DIGIT
NON_ZERO_DIGIT ::= 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
DIGIT_SEQ ::= DIGIT | DIGIT DIGIT_SEQ
----------------------------------------------------------------------------
VAR (*) ::= LETTER | LETTER ALFA_NUM_SEQ
LETTER ::= a | b | c | d | e | f | g | h | i
| j | k | l | m | n | o | p | q | r
| s | t | u | v | w | x | y | z
| A | B | C | D | E | F | G | H | I
| J | K | L | M | N | O | P | Q | R
| S | T | U | V | W | X | Y | Z
ALFA_NUM_SEQ ::= ALFA_NUM | ALFA_NUM ALFA_NUM_SEQ
ALFA_NUM ::= LETTER | DIGIT
----------------------------------------------------------------------------
TYPE ::= Bool | Nat | ( TYPE -> TYPE )
TERM ::= true
| false
| if TERMO then TERMO else TERMO endif
| NUMBER
| suc
| pred
| ehzero 
| VAR
| ( TERM TERM )
| lambda VAR : TYPE . TERM

```

### Custom Types
- `tipo` defines the types `Nat`, `Bool`, and a function type `Seta`.
- `var` represents a variable.
- `termo` encompasses different term types like `True`, `False`, `Numero`, `Suc`, `Pred`, `Eh_zero`, `Var`, `If`, `Lambda`, and `Aplicacao`.

### Type Inference Functions
- `tipar_variavel` checks the type of a variable in the given environment.
- `tipar` infers the type of the term in the provided environment.
- `para_tipo` converts a string to a corresponding type.
- `parser` parses the given symbols and generates the corresponding term.

### Utility Functions
- `invalidar` checks if a variable name is valid.
- `printar_tipo` prints the inferred type of the given term.

### Main Program
The main program reads input from the user, parses the input string, infers the type of the term, and prints the result.
If the input has a term and the term has a type, it shows the type. If the input has a term, but the term does not have a type, it shows '-'. If there is no term, it shows '!'.

## Running the Program

The program requires valid input in the Simply Typed Lambda Calculus format. Upon execution, the program provides the inferred type of the provided term.

For any issues or errors, appropriate error messages are displayed for better understanding and debugging.

---
*This README provides a summary of the implementation of type inference in OCaml for the Simply Typed Lambda Calculus.*
