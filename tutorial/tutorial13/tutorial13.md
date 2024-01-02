---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial 13
2024.1.2

---

# homework

![](./img/eigenspace.png)

---
# homework

C
![](./img/C.png)

$[J]_{B',B}=[2\ 0\ \dfrac{2}{3} 0]$
$Ker(J) = ?$

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
- $\mathbf{x}\in null(A-\lambda I)$
- $\mathbf{x}$ : the eigenvectors(特征向量) of $A$ corresponding to $\lambda$
- $null(A-\lambda I)$ : the eigenspace(特征空间) of $A$ corresponding to $\lambda$

The number of the eigenvectors of $A$ corresponding to $\lambda_i$ is same as the multiplicity of roots of $\lambda_i$ of $p(\lambda)$

---

# property
![](./img/eigenvalue_property.png)

---

# example
$A$ is a $2\times 2$ matrix with eigenvalues $\lambda_1,\lambda_2\in\mathbb{Z}$, $B=A^{-2}-6A^{-1}$, the eigenvalues of $B$ are $-5$ and $7$, find $\lambda_1,\lambda_2$

$\dfrac{1}{\lambda_1^2} - 6\dfrac{1}{\lambda_1} = -5$
$\dfrac{1}{\lambda_2^2} - 6\dfrac{1}{\lambda_2} = 7$

$\lambda_1 = 1, \lambda_2 = -1$

---

# similarity invariants 相似不变量
$B=P^{-1}AP$
- determinant, rank, nullity, trace
- $A$,$B$有相同的特征多项式(eigen polynomial)
    $|\lambda I-B|=|\lambda P^{-1}IP- P^{-1}AP|=|P^{-1}(\lambda I-A)P|=|\lambda I-A|$ 
- $A$,$B$有相同的特征值(eigenvalues)
- $A$,$B$ 特征空间的**维度数**相同,特征空间不一定相同

---

# similarity
$B=P^{-1}AP$
- $A,B$ 有相同的eigenvalues $\lambda$
- 若$\mathbf{x}$是$A$的eigenvector, 则$P^{-1}\mathbf{x}$是$B$的eigenvector
- 若$\mathbf{y}$是$B$的eigenvector, 则$P\mathbf{y}$是$A$的eigenvector

---

# (相似)对角化 Diagonalization
若一个矩阵$A$可写作$D=P^{-1}AP$,即$A=PDP^{-1}$, 则称$A$可对角化(diagonalizable)

usage:
$A^n=PDP^{-1}PDP^{-1}\cdots PDP^{-1}=PD^nP^{-1}$

---

# Diagonalization
e.g. $A=\begin{bmatrix}1&1\\-2&4\end{bmatrix}$, find $A^n$

思路: 将$A$对角化, $A=PDP^{-1}$, $A^n=PD^nP^{-1}$

1. 求$A$的特征值和特征向量
2. 将特征向量组成$P$
原因: $A=PDP^{-1}\Leftrightarrow AP=PD$

$D=diag(\lambda_1,\lambda_2,\cdots,\lambda_n)$
$P=[\mathbf{x}_1,\mathbf{x}_2,\cdots,\mathbf{x}_n]$

$P=\begin{bmatrix}1&1\\-2&4\end{bmatrix}$, $D=\begin{bmatrix}2&0\\0&3\end{bmatrix}$

---

# Diagonalization

可对角化: 对于一个有着$k$重根的特征值, 其特征空间的维度也为$k$

即能找到$n$个线性无关的特征向量

- 若 $A \in M_{n\times n}$拥有$n$个不同的特征值，那么$A$可对角化
    每个特征值至少有一个对应的特征向量

- 不同特征值的对应的特征向量线性无关

- $A$的任何一个特征值$\lambda$, 几何重数(geometric multiplicity)(特征空间的维度) $\leq$ 代数重数(algebraic multiplicity)($\lambda$的重数)

---

# property

- **对称矩阵**不同特征值对应的特征向量彼此正交
    设$\lambda_1\neq \lambda_2$, 其对应的特征向量为$\mathbf{x}_1,\mathbf{x}_2$
    $A\mathbf{x}_1=\lambda_1\mathbf{x}_1,A\mathbf{x}_2=\lambda_2\mathbf{x}_2$
    $\mathbf{x}_1^{\top}A\mathbf{x}_2=\mathbf{x}_1^{\top}\lambda_2\mathbf{x}_2=\lambda_2\mathbf{x}_1^{\top}\mathbf{x}_2$
    $(A\mathbf{x}_1)^{\top}\mathbf{x}_2=(\lambda_1\mathbf{x}_1)^{\top}\mathbf{x}_2$
    $(\lambda_2-\lambda_1)\mathbf{x}_1^{\top}\mathbf{x}_2=x_1^{\top}A\mathbf{x}_2-x_1^{\top}A^{\top}\mathbf{x}_2=0$

- 若将**对称矩阵**的特征向量的基**单位化**得到$P$,则$P$是正交矩阵
    $P^{\top}P=I$

- 实对称矩阵一定可以相似对角化

- $A^{\top}A$的特征值一定都是非负的
    $\forall x, x^{\top}A^{\top}Ax=\|Ax\|^2\geq 0\Leftrightarrow A^{\top}A \succeq 0\Leftrightarrow A^{\top}A$的特征值都是非负的

- 同理, $AA^{\top}$的特征值一定都是非负的

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

# 内积，正交矩阵与二次型
> chapter 6

---

$S = \{\mathbf{u}_1,\mathbf{u}_2,\cdots,\mathbf{u}_n\}$
- orthogonal set(正交集合)
    $\mathbf{u}_i^{\top}\mathbf{u}_j=0$ for $i\neq j$
- **orthogonal normal set / orthonormal**(正交规范集合)
    $S$ is orthogonal and $\|\mathbf{u}_i\|=1$ for $i=1,2,\cdots,n$

- **不包含零向量的正交集合一定是线性无关的**
$\sum\limits_{i=1}^n c_i\mathbf{u}_i=\mathbf{0}\Rightarrow \mathbf{u}_i^{\top}\sum_{i=1}^n c_i\mathbf{u}_i=0\Rightarrow c_i=0$

---

# Orthogonal Matrices(正交矩阵)
- $A^{\top}A=AA^{\top}=I_n$
    $A^{-1}=A^{\top}$


e.g. rotation matrix $R=\begin{bmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{bmatrix}$

---

# 正交矩阵性质
- $A$ 是正交矩阵 $\Leftrightarrow$ $A$ 的行/列向量组成的集合是正交规范集合

- 正交矩阵的行/列向量是**标准正交基底**

- $A$是正交矩阵 $\Leftrightarrow$ $A^{\top}$是正交矩阵

- $A$是正交矩阵 $\Leftrightarrow \|A\mathbf{x}\|=\|\mathbf{x}\|$

- $A$是正交矩阵 $\Leftrightarrow A\mathbf{x}\cdot A\mathbf{y}=\mathbf{x}\cdot\mathbf{y}$

- $A$是正交矩阵 $\Leftrightarrow A^{-1}$也是正交矩阵

- $A,B$是正交矩阵 $\Rightarrow AB$也是正交矩阵

- $A$是正交矩阵 $\Rightarrow |A|=1$ or $|A|=-1$

---

# Orthogonal Diagonalization(正交对角化)

- recall
    若一个矩阵$A$可写作$D=P^{-1}AP$,即$A=PDP^{-1}$, 则称$A$可对角化(diagonalizable)

- 若$P$为正交矩阵, 即$D=P^{\top}AP$, 则称$A$可正交对角化(orthogonal diagonalizable)

---
# 正交对角化
$A$是**实对称**矩阵, 则$A$ 一定可以正交对角化(证明较复杂)

- **对称矩阵**不同特征值对应的特征向量彼此正交(this slide P15)

- 若将**对称矩阵**的特征向量的基**单位化**得到$P$,则$P$是正交矩阵

---

# 内积空间(inner product space)

![](./img/defination.png)

---

# property
![](./img/property.png)

---

# inner product space
![](./img/inner.png)
- 与欧式空间类似, 只需把点乘替换成内积即可$<\cdot,\cdot>$