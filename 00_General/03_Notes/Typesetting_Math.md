
# Typesetting_Math

**Date:** 2026-05-28  
**Subject:** Programming  
**Parent MOC:** [[TODO_LINK_THIS]]  
**Language/Topic:** {{topic}}  
**Source / Reference:**  

---

## Learning Objectives  
-  

---

## Concepts and Definitions  
-  Using `$` as a delimiter encloses inline math expressions
- Using `\[ \]` as delimiters encloses unnumbered, displayed expressions
- Greek alphabet can be represented by using `\alphabet` where alphabet stands for the modern reading of the alphabet, either higher or lowercase, higher case is something more along the lines of `\Alphabet`. Reference the table in the material for the list.
- Commands for operators, functions and other symbols exist and they are all prefixed with `\`
- Math symbols can be negated with `\not`
- Math functions like $\log$ and $\sin$ are by convention represented in standard roman type. For readability
- If a function you'd like to use is not included in the standards, you can define one by using `/mathrm{function}`
- Ellipses are represented by `\ldots` and `\cdots`, where c and l correspond to lower and center respectively
- Commands for arrows also exist. (check material)
- `\frac` is used for representing fractions and it's usage is `\frac{n}{d}`. where n and d are numerator and denominator respectively
- `_` and `^` are for representing super and subscripts respectively, enclosing expressions in curly brackets after them to represent them respectively. For commands like summation, limits, integrals products max and min they are used to represent their parts respectively, if a function used both super and sub it is usually used as `\cmd_{sub}^{super}`
- `\` adds horizontal spacing, there are other commands to add additional spacing (check material), but `\` is the only one that can be used outside of math environments

---

## Code Snippets / Algorithms  
``` insert code here
```
 
---

## Debugging Notes / Common Issues  
-  When using dots, cdots are best used for operators like $\times - + \div$. For example $a_{11} + a_{12} + \cdots + a_{1n}$ 
- Some symbols already have preset negations like \ne for not equals to
- Symbols like + - are represented without commands since they already exist on the keyboard.


---

## Practice Problems / Exercises  
-  

---

## Projects and Implementations  


---

## Questions / Review Points  
-  

---

## Links to Related Notes  

---

## Tags  
#programming #{{topic}} #code #to-review
