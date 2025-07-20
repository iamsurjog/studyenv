---
id: 2_Lexical_Analysis
aliases: []
tags: []
---

# 🔤 2. Lexical Analysis

## 📌 Role of the Lexical Analyzer

- Breaks source code into **tokens**.
    
- Removes whitespace and comments.
    
- Provides a stream of tokens to the syntax analyzer.
    

### 🪙 Token Examples

|Lexeme|Token Type|
|---|---|
|`int`|Keyword|
|`x`|Identifier|
|`+`|Operator|

### 💡 Definitions

- **Lexeme**: Actual sequence of characters.
    
- **Token**: A (token-type, attribute-value) pair.
    
- **Pattern**: A rule describing the structure of lexemes.
    

## 🧾 Regular Expressions for Tokens

Used to define token formats:

- Identifier: `[a-zA-Z_][a-zA-Z0-9_]*`
    
- Integer Constant: `[0-9]+`
    

## 🛠️ Lexical Analyzer Tools

- **Lex/Flex**: Scanner generators.
    
- Often used with **Yacc/Bison** for parsing.
    

## ⚠️ Lexical Errors

- Illegal characters: `@`, `$` (depending on language)
    
- Unclosed string literals
    
- Malformed identifiers
    

## 📝 Class Insight

> DFA implementation for identifiers and number recognition discussed extensively. A state diagram was built for the same.

---
