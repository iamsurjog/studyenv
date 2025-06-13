---
id: 1_Introduction_to_Compilers
aliases: []
tags: []
---

# 🧭 1. Introduction to Compilers

## 📌 What is a Compiler?

A **compiler** is a software tool that translates programs written in high-level programming languages (like C or Java) into low-level machine code or intermediate code that a computer can execute.

### 🔍 Why Do We Need Compilers?

- Bridges human-readable code and hardware-executable instructions.
    
- Performs optimizations for speed and memory usage.
    
- Abstracts platform-specific differences.
    

### ⚖️ Compilation vs. Interpretation

|Feature|Compiler|Interpreter|
|---|---|---|
|Execution|Whole program at once|Line-by-line|
|Speed|Faster after compilation|Slower due to real-time parsing|
|Error Handling|All at once (compile time)|One-by-one (runtime)|

### 🧠 Real-Life Analogy

> A compiler is like a translator who rewrites an entire English book into French before giving it to a reader. An interpreter reads the English book and translates it into French on the spot, line by line.

## 🧩 Phases of a Compiler

Each phase contributes a specific task to the overall compilation process:

1. **Lexical Analysis** – Tokenizes source code.
    
2. **Syntax Analysis** – Parses tokens into a tree structure.
    
3. **Semantic Analysis** – Checks correctness of meaning and types.
    
4. **Intermediate Code Generation** – Converts to a platform-independent representation.
    
5. **Optimization** – Improves performance or reduces code size.
    
6. **Code Generation** – Produces target machine code.
    
7. **Error Handling** – Manages errors encountered during compilation.
    
8. **Symbol Table Management** – Tracks identifiers and their attributes.
    

## 📚 History of Compilers

- First compiler: FORTRAN, developed in 1957 by IBM.
    
- Modern compilers include GCC, LLVM, and Java's javac, supporting various languages and optimizations.
    

---

