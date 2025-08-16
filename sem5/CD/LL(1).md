# Sample Q
E -> E+T|T
T -> T\*F|F
F -> (E)
F -> id

## Answer
### Step 1: remove left recursion and left factoring
E -> TE'
E' -> +TE' | $\varepsilon$
T -> FT'
T' -> \*FT' | $\varepsilon$
F -> (E)
F -> id

### Step 2: Generate First and Follow

| Non Terminal | First             | Follow    |
| :----------: | :---------------- | :-------- |
|      E       | (, id             | (, id     |
|      E'      | +, $\varepsilon$  | follow(E) |
|      T       | (, id             |           |
|      T'      | \*, $\varepsilon$ |           |
|      F       | (, id             |           |