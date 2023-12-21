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
$[T(\mathbf{v})]_{B'}=[T]_{B',B}[\mathbf{v}]_{B}$

---

# Matrices for general linear transformations

为$T$关于基底$B$与$B'$的矩阵表示 
(The matrix for $T$ relative to $B$ and $B'$)

$T_A\Rightarrow [T]_{B',B}$
$B=\{\mathbf{v}_1,\mathbf{v}_2,\cdots,\mathbf{v}_n\}$, $B'=\{\mathbf{w}_1,\mathbf{w}_2,\cdots,\mathbf{w}_m\}$

$[T_A(\mathbf{v})]_{B'}=[T]_{B',B}[\mathbf{v}]_{B}$

$[T]_{B',B}=[[T(\mathbf{v}_1)]_{B'}\ \cdots\ [T(\mathbf{v}_n)]_{B'}]$

- $rank(T) = rank([T]_{B′,B}), nullity(T) = nullity([T]_{B′,B})$

- $[T^{-1}]_{B,B'}=([T]_{B',B})^{-1}$

---

# Matrices for general linear transformations
![w:35cm](./img/example.png)

---

# composition of linear transformations
![w:100cm](./img/composition.png)
$T_1:U\to V, T_2:V\to W$
$[T_2\circ T_1]_{B',B}=[T_2]_{B',B''}[T_1]_{B'',B}$
> cancel the nearest basis(B'')

---

![](./img/property1.png)


---

# inverse of linear transformations
![w:100cm](./img/inverse.png)
$[T^{-1}]_{B,B'}=([T]_{B',B})^{-1}$

---

# property

![](./img/property2.png)

T是一个一一映射 $\Leftrightarrow$ $[T]_{B',B}$ 可逆

---

# theorem
![](./img/theorem.png)

---

# 相似矩阵 Similarity






---

# 特征值(eigenvalue)与特征向量(eigenvector)
> chapter 5 in the textbook

![](./img/eigen.png)

---

# 特征值(eigenvalue)
$A\mathbf{x}=\lambda\mathbf{x}$
$(\lambda I-A)\mathbf{x}=\mathbf{0}$

$\mathbf{x}\neq\mathbf{0}$
$\big|\lambda I-A\big|=0$

- $p(\lambda)=\big|\lambda I-A\big|$: eigen polynomial 特征多项式
- $p(\lambda)=0$: characteristic equation 特征方程

---

# eigen polynomial 特征多项式
$p(\lambda)=\big|\lambda I-A\big|$
$p(\lambda)$为关于$\lambda$,最高次项为$n$的多项式
$p(\lambda)=(\lambda-\lambda_1)\cdots(\lambda-\lambda_n)=\lambda^n+a_{n-1}\lambda^{n-1}+\cdots+a_1\lambda+a_0$

- let $\lambda=0$, then $p(0)=\big|-A\big|=(-1)^n\lambda_1\cdots\lambda_n=a_0\Rightarrow a_0=(-1)^n|A|$
$|A|=\lambda_1\cdots\lambda_n=(-1)^na_0$

- 由行列式的另一种定义(不同行不同列的元素的积之和), $\lambda_{n-1}$的系数只能由$(\lambda-a_{11})\cdots(\lambda-a_{nn})$产生, 即$a_{n-1}=-(a_{11}+\cdots+a_{nn})$
$tr(A)=a_{11}+\cdots+a_{nn}=-a_{n-1}$

---

# 特征向量(eigenvector)
$A\mathbf{x}=\lambda\mathbf{x}$
$(A-\lambda I)\mathbf{x}=\mathbf{0}$
$\mathbf{x}\neq\mathbf{0}$

- the nontrivial solutions of $(A-\lambda I)\mathbf{x}=\mathbf{0}$
- the basis of $null(A-\lambda I)$
- called the eigenvectors of $A$ corresponding to $\lambda$

The number of the eigenvectors of $A$ corresponding to $\lambda_i$ is same as the multiplicity of roots of $\lambda_i$ of $p(\lambda)$

---

# eigenvalue and eigenvector
$A=\begin{bmatrix}0&0&-2\\
1&2&1\\
1&0&3\end{bmatrix}$

find the eigenvalues and eigenvectors of $A$

---

# property
![](./img/eigenvalue_property.png)

---

# example
$A$ is a $2\times 2$ matrix with eigenvalues $\lambda_1,\lambda_2\in\mathbb{Z}$, $B=A^{-2}-6A^{-1}$, the eigenvalues of $B$ are $-5$ and $7$, find $\lambda_1,\lambda_2$

---

# example
$A$ is a $2\times 2$ matrix with eigenvalues $\lambda_1,\lambda_2\in\mathbb{Z}$, $B=A^{-2}-6A^{-1}$, the eigenvalues of $B$ are $-5$ and $7$, find $\lambda_1,\lambda_2$

$\dfrac{1}{\lambda_1^2} - 6\dfrac{1}{\lambda_1} = -5$
$\dfrac{1}{\lambda_2^2} - 6\dfrac{1}{\lambda_2} = 7$

$\lambda_1 = 1, \lambda_2 = -1$

---

# similarity invariants 相似不变量


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

实对称矩阵一定可以相似对角化

$A^{\top}A$的特征值一定都是非负的







