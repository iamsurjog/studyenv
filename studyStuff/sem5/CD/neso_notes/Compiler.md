---
id: Compiler
aliases: []
tags: []
---

# Phases

## Front end
Same everywhere

we can use LANCE for the whole thing
### [[/sem5/CD/neso_notes/Lexical Analysis|Lexical Analysis]]
It takes Lexemes as inputs and generates tokens

let us take the exp:
$x=a+b*c$

| Lexemes |  Tokens  |
| ------- | -------- |
|    x    |identifier|
|    =    |operator  |
|    a    |identifier|
|    +    |operator  |
|    b    |identifier|
|    *    |operator  |
|    c    |identifier|

Regex for identifiers: l(l+d)^* \| _(l+d)^*
l -> letters
d -> digits

we can use LEX

###  [[/sem5/CD/neso_notes/Syntax Analysis|Syntax Analysis]]
Also known as parser

uses context free grammer

production rules:
S -> id = E;
E -> E + T|T
T -> T * F|F
F -> id

id -> identifiers

Produces a parse tree

we can use YACC

###  [[/sem5/CD/neso_notes/Semantic Analysis|Semantic Analysis]]

Produces semantically verfied parse tree

it checks type checking, array bound checking and correctness of scope resolution

type mismatch, undeclared vars, misuse of reserved words, multiple declaration of var in single scope, accessing out of scope var, mismatch between formal and actual params, etc

### [[/sem5/CD/neso_notes/Intermediate Code generation|Intermediate Code generation]]

Produces intermediate code

t<sub>0</sub> = b * c
t<sub>1</sub> = a + t<sub>0</sub>
x = t<sub>1</sub>


## Back end
Changes for different OS
### [[/sem5/CD/neso_notes/Code Optimization|Code Optimization]]

converts the above code to 

t<sub>0</sub> = b * c
t<sub>1</sub> = a + x

### [[/sem5/CD/neso_notes/Target Code Generation|Target Code Generation]]

produces assembly code

```
mov eax, DWORD PTR [rbp-8]
imul eax, DWORD PTR [rbp-12]
mov edx, eax
mov eax, DWORD PTR [rbp-4]
add eax, edx
mov DWORD PTR [rbp-16], eax
```


# Additional parts

## [[/sem5/CD/neso_notes/Symbol_Table|Symbol Table]]


## [[/sem5/CD/neso_notes/Symbol_Table|Error Handler|Error Handler]]
