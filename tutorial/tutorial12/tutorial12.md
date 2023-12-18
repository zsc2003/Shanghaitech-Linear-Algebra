---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial 12
2023.12.26

---

# homework


---

# 线性变换的矩阵表示
Matrices for general linear transformations

![w:20cm](./img/matrix.png)

为$T$关于基底$B$与$B'$的矩阵表示 
(The matrix for $T$ relative to $B$ and $B'$)

$[T]_{B',B}=[[T(\mathbf{v}_1)]_{B'}\ \cdots\ [T(\mathbf{v}_n)]_{B'}]$

---

# Matrices for general linear transformations








---

# 特征值(eigenvalue)与特征向量(eigenvector)
> chapter 5 in the textbook











---

# 对角化 Diagonalization







---

# 数列的特征值

e.g. $a_0=a_1=1,a_{n+2}=a_{n+1}+a_n$

$x^2 = x + 1$
$x_1 = \frac{1+\sqrt{5}}{2},x_2 = \frac{1-\sqrt{5}}{2}$
$a_n = c_1x_1^n + c_2x_2^n$
带入$a_0=a_1=1$得到$c_1,c_2$的值
$c_1=\frac{1}{\sqrt{5}},c_2=-\frac{1}{\sqrt{5}}$
所以$a_n = \frac{1}{\sqrt{5}}(\frac{1+\sqrt{5}}{2})^n - \frac{1}{\sqrt{5}}(\frac{1-\sqrt{5}}{2})^n$

---

# 数列的特征值

e.g. $a_0=a_1=1,a_{n+2}=a_{n+1}+a_n$
$$\begin{bmatrix}a_{n+2}\\a_{n+1}\end{bmatrix} = \begin{bmatrix}1&1\\1&0\end{bmatrix}\begin{bmatrix}a_{n+1}\\a_{n}\end{bmatrix}$$
$$\begin{bmatrix}a_{n+2}\\a_{n+1}\end{bmatrix} = \begin{bmatrix}1&1\\1&0\end{bmatrix}^n\begin{bmatrix}a_{1}\\a_{0}\end{bmatrix}$$
对$\begin{bmatrix}1&1\\1&0\end{bmatrix}$做特征值分解:
$\big|\begin{matrix*}1-\lambda&1\\1&-\lambda\end{matrix*}\big| = \lambda^2-\lambda-1=0$

$$\begin{bmatrix}1&1\\1&0\end{bmatrix} = \begin{bmatrix}\frac{1+\sqrt{5}}{2}&\frac{1-\sqrt{5}}{2}\\\frac{1-\sqrt{5}}{2}&\frac{1+\sqrt{5}}{2}\end{bmatrix}\begin{bmatrix}\frac{1+\sqrt{5}}{2}&0\\0&\frac{1-\sqrt{5}}{2}\end{bmatrix}\begin{bmatrix}\frac{1}{\sqrt{5}}&\frac{1}{\sqrt{5}}\\-\frac{1}{\sqrt{5}}&\frac{1}{\sqrt{5}}\end{bmatrix}$$


---

# 相似矩阵 Similarity







