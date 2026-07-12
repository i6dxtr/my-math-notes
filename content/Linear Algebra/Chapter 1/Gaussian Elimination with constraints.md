 #ch1
- essentially, following the normal steps to achieve [[Row Echelon Form]] i.e. using the row operations, but to find the general solution, we need to work with the constraints:

> [!example]
> $$
> > \begin{align}
> &\text{Find the general solution for the following matrix: }
> \left(\begin{array}{ccc|c}
> a & 0 & b & 2 \\
> a & 2 & a & b \\
> b & 2 & a & a
> \end{array}\right) \\
> &\text{Solution:} \\
> &\rightarrow _{R_{3}\rightarrow \frac{-b}{a}R_{1}+R_{3}}
>
> \left(\begin{array}{ccc|c}
> a & 0 & b  & 2\\
> 0 & 2 & a-b & b-2 \\
> 0 & 2 & \frac{a-b^{2}}{a} & a-\frac{2b}{a}
> \end{array}\right)\rightarrow  \\
> &\text{Perform a row operation to elimate the }(2,0)\text{-entry}\\
>
> &\left(\begin{array}{ccc|c}
> a & 0 & b & 2 \\
> 0 & 2 & a-b & b-2 \\
> 0 & 0 & b-\frac{b^{2}}{a}  & a-\frac{2b}{a}-b +2
> \end{array}\right)\rightarrow \\
> &\text{No solution}: \\
> b&=\frac{b^{2}}{a}\text{ and non-zero} \\
> a&=\frac{b^{2}}{b}=b
> \end{align}
> $$

> [!remark]
> - Observe the last row:
> 	- Solving for $b$ gives above solution
> 	- Solving for $a$ gives second solution s.t. $a=b$
> 	- Substituting second for first gives $b=b$
> 		- Case $b=0$ means no solution
> 		- Otherwise has exactly 1 solution

- Observe the conditions where a pivot is augmented such that it changes the number of solutions
	- Make case for each:

> [!example]
> $$
> > \begin{align}
> \text{Case 1: }a=0 \\
> \left(\begin{array}{ccc|c}
> 0 & 0 & b & 2 \\
> 0 & 2 & 0 & b \\
> b & 2 & 0 & 0
> \end{array}\right)\\
> \left(\begin{array}{ccc|c}
> b & 2 & 0 & 0 \\
> 0 & 2 & 0 & b \\
> 0 & 0 & b & 2
> \end{array}\right) \\
> b&=0\longrightarrow\text{No solution} \\
> b&\neq 0\longrightarrow\text{ Unique solution}
> \end{align}
>
> $$

