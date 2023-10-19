---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial 3
2023.10.24

---

# homework




---


# Diagonal matrices

- for diagonal matrix $D$, $D_{ij} = 0$ for $i \neq j$
so it can be written as $D = diag(d_1, d_2, \cdots, d_n)$

- the power of diagonal matrix is easy to compute
$D^k = diag(d_1^k, d_2^k, \cdots, d_n^k)$
$\to$ similarity and diagonalizable(much later)

- the diagonal matrix $D$ is invertible if and only if $d_i \neq 0$ for all $i$

---

# triangular matrix


---

# symmetric matrix
- $A^T=A$

all properties of symmetric matrix are based on this definition(this time)
(more propertires later such as similarity and diagonalizable)

- $\forall A_{m\times n}, AA^T$ or $A^TA$ are symmetric matrix

---

# determinant
- a function mapping a matrix $A$ into a scalar $det(A)$ or $|A|$
$A^{-1} = \frac{1}{|A|}A^*$

- the most simple usage: invertibility

---

# minor and cofactor


![](./img/matrix.png) ![](./img/matrix_del.png)

- minor: 余子式 $\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ M_{ij} = det(\tilde{A}_{ij})$
- cofactor: 代数余子式 $\ \ \ \ \ \ \ \ \ \ \ \ \ C_{ij}=(-1)^{i+j}M_{ij}$ 

- cofactor expansion along the i-th row
$det(A)=\sum\limits_{j=1}^na_{ij}C_{ij}$
- similarly, we can expand along the j-th column

---

# determinant example
![](./img/determinant_example.png)

- expand along the row?
- expand along the column?

---

# trangular matrix determinant
$A=\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
0 & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & a_{nn}
\end{bmatrix}$

- $det(A) = \prod\limits_{i=1}^na_{ii}$

- and the lower triangular matrix is the same

---

# determinant properties

1. 


$|A^T|=|A|$
$\lambda A = \lambda^n|A|$
$|AB|=|A||B|$
$|A^{-1}|=\frac{1}{|A|}$













---

# Vandermonde determinant
$V=\begin{bmatrix}
1 & x_1 & x_1^2 & \cdots & x_1^{n-1} \\
1 & x_2 & x_2^2 & \cdots & x_2^{n-1} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & x_n & x_n^2 & \cdots & x_n^{n-1}
\end{bmatrix}$
- $det(V) = \prod\limits_{1\leq i < j \leq n}(x_j-x_i)$

proof: induction
- verify $n=3$

> https://blog.csdn.net/u011089523/article/details/72845136

---

![](./img/vandermonde.png)

