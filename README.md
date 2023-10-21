# Type Inference Implementation

This project involves the implementation of a type inference program in OCaml. The program is designed to analyze terms from the Simply Typed Lambda Calculus and determine their types. The README provides an overview of the code structure and functionality.
Code Structure
Custom Types

    tipo defines the types Nat, Bool, and a function type Seta.
    var represents a variable.
    termo encompasses different term types like True, False, Numero, Suc, Pred, Eh_zero, Var, If, Lambda, and Aplicacao.

Type Inference Functions

    tipar_variavel checks the type of a variable in the given environment.
    tipar infers the type of the term in the provided environment.
    para_tipo converts a string to a corresponding type.
    parser parses the given symbols and generates the corresponding term.

Utility Functions

    invalidar checks if a variable name is valid.
    printar_tipo prints the inferred type of the given term.

Main Program

The main program reads input from the user, parses the input string, infers the type of the term, and prints the result.
Running the Program

The program requires valid input in the Simply Typed Lambda Calculus format. Upon execution, the program provides the inferred type of the provided term.

For any issues or errors, appropriate error messages are displayed for better understanding and debugging.
