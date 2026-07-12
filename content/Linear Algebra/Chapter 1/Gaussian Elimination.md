 #ch1
- uses the [[Row Operations]] for a [[Matrix]] to place them in [[Row Echelon Form]]
	- the [[Row Echelon Form]] page also has more examples
#### Regular Case
$$
M=(A\ |\ \overline{b})=
\left(\begin{array}{cccc|c}
a_{11} & a_{12} & ... & a_{1n} & b_{1}  \\
a_{21} & a_{22} & ... & a_{2n} & b_{2} \\
... & ... & ... & ... & ... \\
a_{m1} & a_{m2} & ... & a_{mn} & b_{m}
\end{array}\right)
$$
- $m \times (n+1)$ [[Matrix]], made by simply attaching right-hand-side vector onto original coefficient matrix:
	$$
	\begin{align}
	x+2y+z&=2 \\
	3x+6y+z&=7 \\
	x+y+4z&=3 \\ \\
	&=
	\left(\begin{array}{ccc|c}
	1 & 2 & 1 & 2 \\
	2 & 6 & 1 & 7 \\
	1 & 1 & 4 & 3
	\end{array}\right)
	\\
	\end{align}
	$$
- same number of equations $n$ as unknowns

> [!remark]
> When elementary row operation of scalar multiple addition of a row to another is performed, it is important that the result replaces the row being added to, *not* the row being multiplied by the scalar.

> [!example]
> $$
> > \begin{align}
> &\left(\begin{array}{ccc|c}
> 1 & 2 & 1 & 2 \\
> 2 & 6 & 1 & 7 \\
> 1 & 1 & 4 & 3
> \end{array}\right)
> && R2 +-2 \times R1, \ R3-R1,\ R3+\frac{1}{2}R2 && \longrightarrow
> \left(\begin{array}{ccc|c}
> 1 & 2 & 1 & 2 \\
> 0 & 2 & -1 & 3 \\
> 0 & 0 & \frac{5}{2}& \frac{5}{2}
> \end{array}\right) \\ \\
> N&=(U\ |\ \overline{c}), \text{ where }&&U=\begin{pmatrix} 1 & 2 & 1\\0 & 1 & -1\\0 & 0 & \frac{5}{2} \end{pmatrix}, &&\overline{c}=\begin{pmatrix} 2\\3\\\frac{5}{2} \end{pmatrix}
> \end{align}
>
> $$
> The corresponding linear system has vector form: 
> $$
> U\ \overline{x}=\overline{c}.
> $$

- $U$ is *upper triangular*

