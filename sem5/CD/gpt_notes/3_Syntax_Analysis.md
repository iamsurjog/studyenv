---
id: 3_Syntax_Analysis
aliases: []
tags: []
---

# 🌲 3. Syntax Analysis

## 📌 Objective

To verify the syntactical structure of the token stream using formal grammar rules.

## 🧮 Context-Free Grammar (CFG)

Defines syntax of programming languages.

- Example: `S -> aSb | ε`
    

### 🧱 Components

- **Terminals**: Tokens like `int`, `+`, `;`
    
- **Non-terminals**: Abstract syntactic variables like `Expr`
    
- **Start Symbol**: Usually the program's main structure
    
- **Productions**: Derivation rules
    

## 🌳 Parse Trees

- Graphical representation of derivation.
    
- Leaves = terminals; internal nodes = non-terminals.
    

## 📚 Parsing Techniques

### 🔼 Top-Down Parsing

- Begins at the root (start symbol)
    
- Techniques: Recursive Descent, LL(1)
    

### 🔽 Bottom-Up Parsing

- Begins at the leaves (tokens)
    
- Techniques: LR(0), SLR(1), LALR(1)
    

### 🚨 Ambiguous Grammar

A grammar is ambiguous if more than one parse tree exists for a single input string.

## 📝 Class Insight

> Created LL(1) parsing tables for a simple arithmetic grammar. Required for mid-semester exams.

---
