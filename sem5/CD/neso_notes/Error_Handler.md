2 Types of errors:
Runtime and compile time

## Compile time error
### [[/sem5/CD/neso_notes/Lexical_Errors|Lexical Error]]
 - Identifiers are way too long
 - Exceeding length of numeric constant
 - Numeric constants are ill-formed
	 - (123$123)
 - Illegal characters that are absent from the source code

#### Recovery:
 - Panic mode recovery: after error, chars are escaped until delimiter is found
 - Transpose of two adjacent chars
 - Insert a missing char
 - Delete an unknown or extra char
 - Replace a char with another



### Syntactical Errors


### Semantic Errors
