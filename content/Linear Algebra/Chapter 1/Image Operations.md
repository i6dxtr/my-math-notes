 #ch1
Performing the [[Matrix Operations]] on a given image produces various different visual results:
	- **Scalar multiplication and vector addition**:
	- $\mathbb{R}^{n}:{ \langle x_{1}, i, x_{a} \rangle, x_{1},...,x_{n} \in \mathbb{R}}$
	- $M_{m},n$=$m\cdot n$ matrices with real entries
	- Addition is component wise:
$$
\begin{pmatrix}
x_{1} \\
...  \\
x_{n}
\end{pmatrix}+
\begin{pmatrix}
y_{1} \\
... \\
y_{u}
\end{pmatrix}
=\begin{pmatrix}
x_{1}+y_{1} \\
... \\
x_{n}+y_{u}
\end{pmatrix}
$$
	- Vector addition $\longrightarrow$ controls contrast
		- Pixel value above mean = add to brightness
		- Pixel value below mean = opposite