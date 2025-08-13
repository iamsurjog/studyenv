---
id: SLR Parser
aliases: []
tags: []
---

# Q sample
E -> E + T
E -> T
T -> T * F
T -> F
F -> (E)
F -> id

## Answer
### Step 1: Augmented Grammer
E' -> E
E -> E+T
E -> T
T -> T * F
T -> F
F -> (E)
F -> id
### Step 2: Canonical LR(0) Collection
#### $I_0$:
E' ->.E
E -> .E+T
E -> .T
T -> .T * F
T -> .F
F -> .(E)
F -> .id

#### Goto($I_0$, E) -> $I_1$:
E' -> E.
E -> E.+T
#### Goto($I_0$, T) -> $I_2$:
E -> T.
E -> T.* F
#### Goto($I_0$, F) -> $I_3$:
T -> F.
#### Goto($I_0$, "(") -> $I_4$:
F -> (.E)
E -> .E+T
E -> .T
T -> .T * F
T -> .F
F -> .(E)
F -> .id
#### Goto($I_0$, id) -> $I_5$:

F -> id.
#### Goto($I_1$, +) -> $I_6$:
E -> E+.T
T -> .T * F
T -> .F
F -> .(E)
F -> .id
#### Goto($I_2$, \*) -> $I_7$:
T -> T*.F
F -> .(E)
F -> .id
#### Goto($I_4$, E) -> $I_8$:
F -> (E.)
E -> E.+T
#### Goto($I_6$, T) -> $I_9$:
E -> E+T.
T -> T. * F
#### Goto($I_7$, F) -> $I_{10}$:
T -> T\*F.
#### Goto($I_8$, ")") -> $I_{11}$:
F -> (E).

### Step 4: First and Follow
| State | FIrst | Follow |
| :---: | :---: | :----: |
|   E   |   (   |  +)$   |
|   T   |   (   | +)\*$  |
|   F   |   (   | +\*)$  |
|       |       |        |

### Step 3: Parser Table

| State |  +  |  *  | id  |  (  |  )  |  $  |  E  |  T  |  F  |
| :---: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|   0   |     |     | s5  | s4  |     |     |  1  |  2  |  3  |
|   1   | s6  |     |     |     |     | Acc |     |     |     |
|   2   | r3  | s7  |     | r3  |     | r3  |     |     |     |
|   3   |     | r5  |     |     |     | r5  |     |     |     |
|   4   |     |     |     |     |     |     |  8  |     |     |
|   5   |     |     |     |     |     | r6  |     |     |     |
|   6   |     |     |     |     |     |     |     |  9  |     |
|   7   |     |     |     |     |     |     |     |     | 10  |
|   8   |     |     |     |     | s11 |     |     |     |     |
|   9   | r2  |     |     | r2  |     | r2  |     |     |     |
|  10   |     | r4  |     |     |     | r4  |     |     |     |
|  11   |     |     |     |     |     | r6  |     |     |     |
