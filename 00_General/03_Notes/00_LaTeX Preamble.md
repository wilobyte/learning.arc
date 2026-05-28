# 00_LaTeX Preamble

**Date:** 2025-06-15  
**Subject:** General
**Parent MOC:** [[TODO_LINK_THIS]]  
**Topic:** LaTeX Preamble
**Source / Reference:**  [Learning LaTeX, Griffiths](obsidian://open?vault=Learning%20Arc&file=00_General%2F01_Resources%2F04_Learning_Latex_Griffiths.pdf)

---

## Learning Objectives  
-  Overview of the $\LaTeX$ typesetting language.

---

## Key Concepts
- LaTeX is computer typesetting system that specializes in producing mathematically oriented documents.  
- LaTeX is not a WYSIWYG type setting system, it's logical. This forces you to think about the structure of the document rather than on the appearance of the end result. 
- LaTeX makes it possible to create an impressive-looking document that's full of errors and inconsistencies. So make sure to check and review your work.
- The command to run LaTeX on `first.tex` is  
```
latex first.tex
```
- The command produces the file `first.dvi`(device independent). This file can be understood by any one of several output devices.
- Files with the extensions `aux` and `log` are also created. (Other files with extensions such as `toc`, `idx`, and `bbl`, may also be generated).
- Always check output is correct before printing by displaying it on the screen. This process is called *previewing*.
- The `dvi` and corresponding `ps` file (if you  converted from `dvi` to PostScript) should be deleted after use but not the `tex` file. 
---

## Links to Related Notes  
- [[01_Basic_LaTeX_Essentials_MOC]]
---

## Tags  
#general #LaTeX #reviewed
