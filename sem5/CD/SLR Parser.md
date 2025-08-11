# Q sample)
E -> E * T
E -> T
T -> T * F
T -> F
F -> (E)
F -> id

## Answer
### Step 1: Augmented Grammer
E' -> E
E -> T
T -> T * F
T -> F
F -> (E)
F -> id
### Step 2: Canonical LR(0) Collection
#### $I_0$:
E' ->.E
E -> .T
T -> .T * F
T -> .F
F -> .(E)
F -> .id

#### Goto($I_0$, E) -> $I_1$:
