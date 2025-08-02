---
id: 5_Intermediate_Code_Generation
aliases: []
tags: []
---

# 🏗️ 5. Intermediate Code Generation

## 📌 Purpose

Translate source-level constructs into an intermediate representation that is independent of hardware.

## 🧾 Common Forms

- **Three Address Code (TAC)**: `a = b + c`
    
- **Postfix Notation**: `bc+`
    
- **Quadruples/Triples**: Structured representations
    

### 🧪 Example

```c
// Original
a = b + c * d;

// TAC
T1 = c * d
T2 = b + T1
a = T2
```

## 📚 Class Exercise

> Translate `x = a * b + c / d - e` into TAC, Quadruples, and Triples. Discussed implications for optimization.

---

