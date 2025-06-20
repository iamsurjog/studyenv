---
id: Symbol_Table
aliases:
  - Symbol Table
tags: []
---

# Symbol Table

eg: int count;
char x[] = "Sujatro";

| Name  | Type | Size | Dimension | Line of Declaration |        Line of usage         | Address |
| :---: | :--: | :--: | :-------: | :-----------------: | :--------------------------: | :-----: |
| count | int  |  2   |     0     |         --          | -- (linked list if multiple) |   --    |
|   x   | char |  7   |     1     |         --          |              --              |   --    |

## Operations:
### Non-block Structured Language
Eg: Fortran

contains single instance of variable declaration

Operations:
Insert()
Lookup()

### Block Structured Language
Eg: Fortran

variable declaration may happen multiple times

Operations:
Insert()
Lookup()
Set()
Reset()
