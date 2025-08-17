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

| Non Terminal | First             | Follow       |
| :----------: | :---------------- | :----------- |
|      E       | (, id             | ), $         |
|      E'      | +, $\varepsilon$  | ), $         |
|      T       | (, id             | +, ), $      |
|      T'      | \*, $\varepsilon$ | +, ), $      |
|      F       | (, id             | \*,  +, ), $ |

### Step 3: Parsing table
| Non Terminal |    id     |         +          |      *      |         (          |  )  |         $          |
| :----------: | :-------: | :----------------: | :---------: | :----------------: | :-: | :----------------: |
|      E       | E -> TE'  |                    |             |      E -> TE'      |     |                    |
|      E'      |           |     E' -> +TE'     |             | E' ->$\varepsilon$ |     | E' ->$\varepsilon$ |
|      T       |  T ->FT'  |                    |             |      T ->FT'       |     |                    |
|      T'      |           | T' ->$\varepsilon$ | T' -> \*FT' | T' ->$\varepsilon$ |     | T' ->$\varepsilon$ |
|      F       | F -> (id) |                    |             |      F -> (E)      |     |                    |
