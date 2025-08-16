# Sample Q:
(a|b)\*abb#

## Answer
### Step 1: Parser tree

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.16 - 17.11pm.drawing",
	"width": 772,
	"aspectRatio": 0.9334945586457074
}
```

### Step 2: Compute nullable, firstpos and followpos
|     Node      | Nullable     | Firstpos                                    | Lastpos                                     |
| :-----------: | ------------ | ------------------------------------------- | ------------------------------------------- |
| $\varepsilon$ | true         | $\Phi$                                      | $\Phi$                                      |
|       i       | false        | {i}                                         | {i}                                         |
|      \|       | n(L) \| n(R) | f(L)$\cup$f(R)                              | l(L)$\cup$l(R)                              |
|    $\cdot$    | n(L) & n(R)  | if n(L):<br>f(L)$\cup$f(R)<br>else:<br>f(L) | if n(R):<br>l(L)$\cup$l(R)<br>else:<br>l(R) |
|       *       | true         | f(L)                                        | l(L)                                        |

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.16 - 21.53pm.drawing",
	"width": 1128,
	"aspectRatio": 1.2547274749721913
}
```

### Step 3: Follow Pos
1. if n is a cat ($\cdot$) node then for every position i  in lastpos(L) all positions in firstpos(R) are in followpos(i)
2. if n is a * node and i is a pos in lastpos(n) then all positions in firstpos(n) are in followpos(i)

| Node | Follow Pos |
| :--: | :--------: |
|  1   | {1, 2, 3}  |
|  2   | {1, 2, 3}  |
|  3   |     4      |
|  4   |     5      |
|  5   |     6      |
|  6   |   $\Phi$   |

### Step 4: Dtran or the transition table
Starting state -> {1, 2, 3}
so 1, 3 give a, and 2 gives b
thus Dtran({1, 2, 3}, a) = Follow(1) $\cup$ Follow(3)
and Dtran({1, 2, 3}, b) = Follow(2)

|    State     |      a       |      b       |
| :----------: | :----------: | :----------: |
|  {1, 2, 3}   | {1, 2, 3, 4} |  {1, 2, 3}   |
| {1, 2, 3, 4} | {1, 2, 3, 4} | {1, 2, 3, 5} |
| {1, 2, 3, 5} | {1, 2, 3, 4} | {1, 2, 3, 6} |
| {1, 2, 3, 6} | {1, 2, 3, 4} |  {1, 2, 3}   |

### Step 5: DFA table

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.16 - 23.09pm.drawing",
	"width": 904,
	"aspectRatio": 1.748549323017408
}
```
