# Syntax Analyzer
 A syntax analyzer for a hypothetical imperative programming language that reads input programs from files and determines if they contain any syntax errors. Implemented in Python.

 # Syntax Analyzer for Hypothetical Imperative Programming Language

This project is a syntax analyzer for a hypothetical imperative programming language. It reads input programs from text files and determines if they contain any syntax errors. The analyzer consists of a lexical analyzer and a parser implemented in Python.

## Features

- **Lexical Analyzer**: Tokenizes the input source code.
- **Parser**: Checks the syntax of the tokenized source code based on predefined EBNF rules.
- **Supports**: Assignment statements, if statements, loop statements, and expressions involving arithmetic and logic operations.

## Grammar Rules

The parser is based on the following EBNF rules:

<program> -> program begin <statement_list> end
<statement_list> -> <statement> {;<statement>}
<statement> -> <assignment_statement> | <if_statement> | <loop_statement>
<assignment_statement> -> <variable> = <expression>
<variable> -> identifier (An identifier is a string that begins with a letter followed by 0 or more letters and/or digits)
<expression> -> <term> { (+|-) <term>}
<term> -> <factor> {(* | /) <factor> }
<factor> -> identifier | int_constant | (<expr>)
<if_statement> -> if (<logic_expression>) then <statement>
<logic_expression> -> <variable> (< | >) <variable> (Assume that logic expressions have only less than or greater than operators)
<loop_statement> -> loop (<logic_expression>) <statement>

Source: Concepts of Programming Languages
12th edition
Robert W. Sebesta
Pearson Education, 2018