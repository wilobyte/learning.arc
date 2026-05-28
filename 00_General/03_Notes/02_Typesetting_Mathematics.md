# 02_Typesetting_Mathematics

**Date:** 2025-06-25  
**Subject:** General
**Parent MOC:** [[02_Typesetting_Mathematics_MOC]]  
**Language/Topic:** LaTeX
**Source / Reference:** [[04_Learning_Latex_Griffiths.pdf]] 

---

## Learning Objectives  
-  Learn about the:
	- Essential commands, 
	- Greek letters,
	- Mathematical Functions, 
	- Arrows and Symbols.
- Learn and implement: 
	- Equation Environments.
	- Using Fonts, Hats, and Underlining
	- Implement Braces, 
	- Matrices and arrays, 
	- Customized Commands, 
	- Theorem-like Environments,
	- Math Miscellany.

---

## Concepts and Definitions  
- 11Notice that mathematical symbols appear in an italic-like font.
- Single dollar signs enclose and in-line mathematical expression.
- The delimeters `\[` and `\]` are used for unnumbered, displayed equations.
- Here's a table containing all the common math symbols and the commands used to produce them:

| Command     | Symbol      | Command    | Symbol     | Command       | Symbol        |
| ----------- | ----------- | ---------- | ---------- | ------------- | ------------- |
| `\alpha`    | $\alpha$    | `\beta`    | $\beta$    | `\gamma`      | $\gamma$      |
| `\delta`    | $\delta$    | `\epsilon` | $\epsilon$ | `\varepsilon` | $\varepsilon$ |
| `\zeta`     | $\zeta$     | `\eta`     | $\eta$     | `\theta`      | $\theta$      |
| `\vartheta` | $\vartheta$ | `\iota`    | $\iota$    | `\kappa`      | $\kappa$      |
| `\lambda`   | $\lambda$   | `\mu`      | $\mu$      | `\nu`         | $\nu$         |
| `\xi`       | $\xi$       | `\pi`      | $\pi$      | `\varpi`      | $\varpi$      |
| `\rho`      | $\rho$      | `\varrho`  | $\varrho$  | `\sigma`      | $\sigma$      |
| `\tau`      | $\tau$      | `\upsilon` | $\upsilon$ | `\phi`        | $\phi$        |
| `\varphi`   | $\varphi$   | `\chi`     | $\chi$     | `\psi`        | $\psi$        |
| `\omega`    | $\omega$    |            |            |               |               |
{Greek lower}

| Command   | Symbol    | Command    | Symbol     | Command  | Symbol   |
| --------- | --------- | ---------- | ---------- | -------- | -------- |
| `\Gamma`  | $\Gamma$  | `\Delta`   | $\Delta$   | `\Theta` | $\Theta$ |
| `\Lambda` | $\Lambda$ | `\Xi`      | $\Xi$      | `\Pi`    | $\Pi$    |
| `\Sigma`  | $\Sigma$  | `\Upsilon` | $\Upsilon$ | `\Phi`   | $\Phi$   |
| `\Psi`    | $\Psi$    | `\Omega`   | $\Omega$   |          |          |
{Greek upper}

| Command    | Symbol     | Command   | Symbol    | Command    | Symbol     |
| ---------- | ---------- | --------- | --------- | ---------- | ---------- |
| `\pm`      | $\pm$      | `\mp`     | $\mp$     | `\times`   | $\times$   |
| `\div`     | $\div$     | `\cap`    | $\cap$    | `\cup`     | $\cup$     |
| `\vee`     | $\vee$     | `\wedge`  | $\wedge$  | `\circ`    | $\circ$    |
| `\ast`     | $\ast$     | `\star`   | $\star$   | `\diamond` | $\diamond$ |
| `\bigcirc` | $\bigcirc$ | `\cdot`   | $\cdot$   | `\odot`    | $\odot$    |
| `\bullet`  | $\bullet$  | `\oplus`  | $\oplus$  | `\ominus`  | $\ominus$  |
| `\otimes`  | $\otimes$  | `\oslash` | $\oslash$ |            |            |


| Command      | Symbol       | Command    | Symbol     | Command     | Symbol      |
| ------------ | ------------ | ---------- | ---------- | ----------- | ----------- |
| `\nabla`     | $\nabla$     | `\|`       | $\|$       | `\prime`    | $\prime$    |
| `\surd`      | $\surd$      | `\partial` | $\partial$ | `\ell`      | $\ell$      |
| `\Re`        | $\Re$        | `\Im`      | $\Im$      | `infty`     | $\infty$    |
| `\triangle`  | $\triangle$  | `\exists`  | $\exists$  | `\forall`   | $\forall$   |
| `\imath`     | $\imath$     | `\jmath`   | $\jmath$   | `\emptyset` | $\emptyset$ |
| `\backslash` | $\backslash$ |            |            |             |             |

| Command   | Symbol    | Command     | Symbol      | Command     | Symbol      |
| --------- | --------- | ----------- | ----------- | ----------- | ----------- |
| `\le`     | $\le$     | `\ll`       | $\ll$       | `\geq`      | $\geq$      |
| `\gg`     | $\gg$     | `\subset`   | $\subset$   | `\subseteq` | $\subseteq$ |
| `\supset` | $\supset$ | `\supseteq` | $\supseteq$ | `\in`       | $\in$       |
| `\ni`     | $\ni$     | `\notin`    | $\notin$    | `\propto`   | $\propto$   |
| `\ne`     | $\ne$     | `\equiv`    | $\equiv$    | `\approx`   | $\approx$   |
| `\sim`    | $\sim$    | `\perp`     | $\perp$     | `\parallel` | $\parallel$ |
| `\cong`   | $\cong$   | `\simeq`    | $\simeq$    |             |             |

| Command     | Symbol      | Command      | Symbol       | Command   | Symbol    |
| ----------- | ----------- | ------------ | ------------ | --------- | --------- |
| `\sum`      | $\sum$      | `\prod`      | $\prod$      | `\int`    | $\int$    |
| `\oint`     | $\oint$     | `\bigcap`    | $\bigcap$    | `\bigcup` | $\bigcup$ |
| `\bigoplus` | $\bigoplus$ | `\bigotimes` | $\bigotimes$ |           |           |
{will scale in size to fit the context}

- A mathematical symbol can be negated using the `\not` command.
- `$\not<$` produces $\not<$
- The commands `\ne` $\ne$ and `\notin` $\notin$ are already provided.
- Mathematical functions like "log" and "sin" are by convention, typeset in the standard roman type.
- This makes expressions easier to read.
- Compare $\sin x$ with $sin x$. 
- The former used `$\sinx$` and the latter used `$sin x$`.
- Here's a table with the builtin functions available:

| Command   | Symbol    | Command   | Symbol    | Command   | Symbol    |
| --------- | --------- | --------- | --------- | --------- | --------- |
| `\arccos` | $\arccos$ | `\cos`    | $\cos$    | `\csc`    | $\csc$    |
| `\exp`    | $\exp$    | `\ker`    | $\ker$    | `\limsup` | $\limsup$ |
| `\min`    | $\min$    | `\sinh`   | $\sinh$   | `\arcsin` | $\arcsin$ |
| `\cosh`   | $\cosh$   | `\deg`    | $\deg$    | `\gcd`    | $\gcd$    |
| `\lg`     | $\lg$     | `\ln`     | $\ln$     | `\Pr`     | $\Pr$     |
| `\sup`    | $\sup$    | `\arctan` | $\arctan$ | `\cot`    | $\cot$    |
| `\det`    | $\det$    | `\hom`    | $\hom$    | `\lim`    | $\lim$    |
| `\log`    | $\log$    | `\sec`    | $\sec$    | `\tan`    | $\tan$    |
| `\arg`    | $\arg$    | `\coth`   | $\coth$   | `\dim`    | $\dim$    |
| `\inf`    | $\inf$    | `\liminf` | $\liminf$ | `\max`    | $\max$    |
| `\sin`    | $\sin$    | `\tanh`   | $\tanh$   |           |           |
- You may need another function like "diag", which is not available.
- In such a case you may use the `\mathrm` command to produce roman type in a mathematical expression.
- For example: `$\mathrm{diag}(1,2,3,\ldots,20)$` which gives $\mathrm{diag}(1,2,3,\ldots,20)$ 
- The ellipsis "$\ldots$" in the previous expression was produced using `\ldots`.
- Another form "$\cdots$", is produced by `\cdots`. This is more suitable for expressions with $= + \times \div$.
- For example $a_{11} + a_{12} + \cdots + a_{1n}$ 
- Here's a table for arrows:

| Command           | Symbol            | Command               | Symbol                | Command        | Symbol         |
| ----------------- | ----------------- | --------------------- | --------------------- | -------------- | -------------- |
| `\leftarrow`      | $\leftarrow$      | `\longleftarrow`      | $\longleftarrow$      | `\downarrow`   | $\downarrow$   |
| `\Leftarrow`      | $\Leftarrow$      | `\Longleftarrow`      | $\Longleftarrow$      | `Downarrow`    | $\Downarrow$   |
| `\rightarrow`     | $\rightarrow$     | `\longrightarrow`     | $\longrightarrow$     | `\uparrow`     | $\uparrow$     |
| `\Rightarrow`     | $\Rightarrow$     | `\Longrightarrow`     | $\Longrightarrow$     | `\Uparrow`     | $\Uparrow$     |
| `\leftrightarrow` | $\leftrightarrow$ | `\longleftrightarrow` | $\longleftrightarrow$ | `\updownarrow` | $\updownarrow$ |
| `\Leftrightarrow` | $\Leftrightarrow$ | `\Longleftrightarrow` | $\Longleftrightarrow$ | `\Updownarrow` | $\Updownarrow$ |
| `\nearrow`        | $\nearrow$        | `\rightleftharpoons`  | $\rightleftharpoons$  | `\searrow`     | $\searrow$     |
| `\swarrow`        | $\swarrow$        | `\mapsto`             | $\mapsto$             | `\nwarrow`     | $\nwarrow$     |
- The `\frac` command is used for formatting fractions.
- It's always followed by two expressions that are enclosed in curly braces (the numerator and the denominator).
- Example: `\frac{1}{2}` $\frac{1}{2}$ 
- The characters `_` and `^` produce subscripts and superscripts respectively.
- An expression using more than one symbol can be used as a superscript or subscript if it is enclosed in curly braces.
- Example: `x_3 + y^{n+2}, \; n = 1,2,\ldots,N` $x_3 + y^{n+2}, \; n = 1,2,\ldots,N$ 
- In the equation above, the command `\;` adds horizontal spacing. 
- Horizontal spacing commands available in math mode include:
	- Regular: $5,4$ 
	- Negative thin: `\!` $5, \! 4$ 
	- Thin: `\,` $5, \, 4$
	- Medium: `\:` $5, \: 4$
	- Thick: `\;` $5, \; 4$
	- Apart from `\,` these can only be used in math mode.
- Example: `$ \sqrt{2} \sin x $` $\sqrt{2} \sin x$ vs `$ \sqrt{2} \, \sin x $` $\sqrt{2} \, \sin x$
- Superscripts and subscripts are treated differently when they are attached to integral, summation, or product symbols or to max, min, inf, or sup.
- Examples: 
	- Inline form:
		- `S_N = \sum_{j=1}^N a_j` $S_N = \sum_{j=1}^N a_j$ 
		- `\int_{x=0}^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}` $\int_{x=0}^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}$ 
		- `\lim_{n\rightarrow\infty} (1+x/n)^n = e^x` $\lim_{n\rightarrow\infty} (1+x/n)^n = e^x$
		- `\max_{1\le x\le 2}x + \frac{1}{x} = \frac{5}{2}` $\max_{1\le x \le2} x + \frac{1}{x} = \frac{5}{2}$
		- `G(x) := \prod_{i=1}^{n} f_i(x)` $G(x) := \prod_{i=1}^n f_i(x)$ 
	- Displayed eqns:
		```latex
		\[
		  S_N = \sum_{j=1}^N a_j
		\]
		```
		
		$$ S_N = \sum_{j=1}^N a_j $$
		
		```latex
		\[
		  \int_{x=0}^\infty e^{-x^2} dx
			   = \frac{\sqrt{\pi}}{2}
		\]
		```
		
		$$ \int_{x=0}^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2} $$
		
		```latex
		\[
		  \lim_{n\rightarrow\infty} 
		  (1+x/n)^n = e^x
		\]
		```
		$$ \lim_{n\rightarrow\infty} (1+x/n)^n = e^x $$
		```latex
		\[
		  \max_{1\le x\le 2}x + 
			  \frac{1}{x} 
				  = \frac{5}{2}
		\]
		```
		$$ \max_{1\le x\le 2}x + \frac{1}{x} = \frac{5}{2} $$
		```latex
		\[
		  G(x) := \prod_{i=1}^{n} f_i(x)
		\]
		```
		$$ G(x) := \prod_{i=1}^{n} f_i(x) $$
---
## Code Snippets / Algorithms  
``` insert code here
```
 
---

## Debugging Notes / Common Issues  
- 

---

## Practice Problems / Exercises  
-  

---

## Projects and Implementations  
- Related project(s):  
  - [Project Name](./Projects/Project_Name/)  

---

## Questions / Review Points  
-  

---

## Links to Related Notes  

---

## Tags  
#programming #{{topic}} #code #to-review
