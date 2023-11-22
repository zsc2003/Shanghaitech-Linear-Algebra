---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial8

2023.11.28

---

# homework





---

# midterm review 期中复习
- 考试时间: 2023.12.6 星期三 8:15~9:55
- 考试地点: 教学中心202
- 考试内容: 第一章到第四章的4.8节（包含）
- 期中考试占总成绩 30%! 
- 试卷为全英文, 不涉及数学的问题可以找监考人员翻译
- 作答中英文均可

> 欢迎大家有问题随时在群里/私聊提问, 尽量不要拖延问题
> 尽早复习，不要等到考前一天才开始复习
> start early!!!

---

# 一些要强调的事情
- **iff** $\Leftrightarrow$ if and only if $\Leftrightarrow$ 当且仅当, 
$\Rightarrow$ 充分性, $\Leftarrow$ 必要性, 都要证
或者全程使用$\Leftrightarrow$等价表述

- free variables
eg. $x_3=s,x_4=r$
**$s,r\in \mathbf{R}$**!

- consistent 有解的
- inconsistent 无解的
- trival solution 平凡解(无解)
- the symbol [] and || 
  [] for matrix, || for determinant

---
# 一些要强调的事情

- 注意公式不要记错了
    - $\left\|\mathbf{v}\right\|=\sqrt{v_1^2+v_2^2+\cdots+v_n^2}$ 不要忘记根号
    - $\cos\theta=\frac{\mathbf{u}\cdot\mathbf{v}}{\left\|\mathbf{u}\right\|\left\|\mathbf{v}\right\|}$ 分母不要忘记开方
    - $proj_{\mathbf{v}}\mathbf{u}=\frac{\mathbf{u}\cdot\mathbf{v}}{\left\|\mathbf{v}\right\|^2}\mathbf{v}$ 分母不要忘记平方,公式背不过的话可以自己考场推一下

$A=\begin{bmatrix}
1 & 0 & 1 \\
0 & 2 & 0 \\
-2 & 0 & 1
\end{bmatrix}$
- $A+I=?,A-I=?$ 注意$I$是单位矩阵,只有对角线上的元素为1!!!
- $P_n$ 所有次数$\leq n$的多项式的集合
  $P_n=\{p(x)=a_0+a_1x+a_2x^2+\cdots+a_nx^n:a_1,\cdots,a_n\in\mathbb{R}\}$

---
# 一些要强调的事情

- 行列式交换两行后，记得要有一个负号
- 关于叉乘
  $\mathbf{u}\times\mathbf{v}=\begin{vmatrix}
  \mathbf{i} & \mathbf{j} & \mathbf{k} \\
  u_1 & u_2 & u_3 \\
  v_1 & v_2 & v_3
  \end{vmatrix}=(u_2v_3-u_3v_2,-(u_1v_3-u_3v_1),u_1v_2-u_2v_1)$
  注意中间有个负号(原因:$a_{12}$的代数余子式的符号是$(-1)^{1+2}$)
- 行列式按行/列的展开时:
  $|A|=\sum\limits_{i=1}^na_{ij}C_{ij}$
  注意$C_{ij}$是$a_{ij}$的**代数余子式**,有一个$(-1)^{i+j}$!!!
- 矩阵没有二项式定理
e.g. $(A+B)^2=A^2+AB+BA+B^2$

---

# review list 复习清单
- chapter1 线性方程组
  - 矩阵
  - 高斯消元
  - 矩阵求逆
- chapter2 行列式
- chapter3 欧氏空间
- chapter4 向量空间
  - 子空间
  - 线性相关、线性无关
  - 基、维数、基变换
  - 行空间、 列空间、 零空间
  - 矩阵的秩、零度、 矩阵基本空间


---

# Plus/Minus Theorem
$V$ is a vector space, $S\subset V$
- If $S$ is an independent set, and $\mathbf{v}\in V, \mathbf{v}\not\in S$, then $S\cup\{\mathbf{v}\}$ is also an **independent set**
> proof by contradiction, suppose that $S\cup\{\mathbf{v}\}$ is linear dependent $\Rightarrow\mathbf{v}=span(S)$

- If $\mathbf{v}\in S$, and $\mathbf{v}$ can be written as a linear combination of other vectors in $S$, then $span(S-\mathbf{v})=span(S)$
> $\mathbf{v}\in S$, WLOG, take $\mathbf{v}=v_1$, consider $\forall\mathbf{w}\in span(S)$, can be writen as linear combination of $\mathbf{v}_2,\cdots,\mathbf{v}_n$

---

# coordinate
$n\geq 1, \dim(V)=n, S=\{\mathbf{v}_1,\cdots,\mathbf{v}_n\}$ is a basis of $V$

- $1.$ for any vector set $M=\{\mathbf{w}_1,\cdots,\mathbf{w}_r\}\subset V$
$M$ is an independent set $\Leftrightarrow$ $[\mathbf{v}_1]_S,\cdots,[\mathbf{v}_r]_S$ are independent set
> proof: set $[\mathbf{v}_i]=(a_{i1},\cdots,a_{in})$, then $\mathbf{v}_i=a_{i1}\mathbf{v}_1+\cdots+a_{in}\mathbf{v}_n$

- $2.$ for vector set $M=\{\mathbf{w}_1,\cdots,\mathbf{w}_n\}\subset V$
  $M$ is the basis of $V\Leftrightarrow$ $[\mathbf{v}_1]_S,\cdots,[\mathbf{v}_n]_S$ is the basis of $\mathbb{R}^n$
  $\Leftrightarrow$ $[\mathbf{v}_1]_S,\cdots,[\mathbf{v}_n]_S$ is the standard basis of $\mathbb{R}^n$
> from $1.$, we know that $M$ is independent $\Rightarrow$ $[\mathbf{v}_1]_S,\cdots,[\mathbf{v}_n]_S$ is independent, so we just need to prove that $span\{[\mathbf{w}_1]_S,\cdots,[\mathbf{w}_n]_S\}=\mathbb{R}^n$

---
# example
![](./img/example.png)

---
# basis' theorem
$V$ is a vector space,$\dim(V)=n$, $S=\{\mathbf{v}_1,\cdots,\mathbf{v}_m\}\subset V$
- $span(S)=V, m>n$, then we can delete some of the vectors in $S$ to get a basis of $V$
- if $S$ is a linear independent set, $m<n$, then we can add some vectors to $S$ to get a basis of $V$
---
# basis' theorem
$V$ is a vector space, $\dim(V)=n$, $W\subset V$ is a subspace.
- let $m=\dim(W)$, then $m\leq n$
- $W=V$ **iff** $m=n$

---

# Change of basis

$V$ is the vector space, $B,B'$ are two bases of $V$
- $B=\{\mathbf{v}_1,\cdots,\mathbf{v}_n\}$
- $B'=\{\mathbf{v}_1',\cdots,\mathbf{v}_n'\}$
If we have $(\mathbf{v})_B=(c_1,\cdots,c_n)$ 
how could we find $(\mathbf{v})_{B'}=(c_1',\cdots,c_n')$?
> as we known that $[\mathbf{v}]_B, [\mathbf{v}]_{B'}$ has the unique expression

---

# Change of basis

- transition matrix(过渡矩阵) $P$
  $P$ is invertible, $P^{-1}$ is called the transition matrix from $B$ to $B'$

- transition matrix from $B$ to $B'$
  $P_{B\to B'}$ or $P_{B'\leftarrow B}$
- transition matrix from $B'$ to $B$
  $P_{B'\to B}$ or $P_{B\leftarrow B'}$
- $P_{B\leftarrow B'}P_{B'\leftarrow B}=I$
> notice that the defination of the transition matrix may be different with some of the Chinese textbooks!!

---

# Change of basis
- We can represent the transition matrix as  $P_{B\to B'}$ or $P_{B'\leftarrow B}$

- $[v]_{B'}=P_{B'\leftarrow B}[v]_{B}$
- $[v]_{B}=P_{B\leftarrow B'}[v]_{B'}$


- method to get the transition matrix
  $[B'|B]\Rightarrow [I|P_{B'\leftarrow B}]$

---

# example of transition matrix
![](./img/transition.png)

---

# Row space, Column space and Null space
$A$ is a $m\times n$ matrix
- row space 行空间
  $row(A)=span\{\mathbf{r}_1,\cdots,\mathbf{r}_m\}$

- column space 列空间
  $col(A)=span\{\mathbf{c}_1,\cdots,\mathbf{c}_n\}$
- null space 零空间
  $null(A)=\{\mathbf{x}\in\mathbb{R}^n:A\mathbf{x}=\mathbf{0}\}$
- left null space 左零空间 
  $null(A^T)=\{\mathbf{x}\in\mathbb{R}^m:A^T\mathbf{x}=\mathbf{0}\}$

> 行空间和零空间互为正交补
> 列空间和左零空间互为正交补

---
# Row space, Column space and Null space

![](img/space_1.png)
> 正交: $col(A)\perp null(A)$, 补: $col(A)+null(A)=\mathbb{R}^n$

---
![](img/space2.png)

---

# Rank, Nullity and Fundamental Matrix Spaces





---
# Geometry review
- detail in tutorial 5

- 平面的一般式
$Ax+By+Cz+D=0$

- 平面的法向量
  $\mathbf{n}=(A,B,C)$

- 空间中一点$(x_0,y_0,z_0)$到平面的距离
  $d=\dfrac{|Ax_0+By_0+Cz_0+D|}{\sqrt{A^2+B^2+C^2}}$

- 过空间内一点$(x_0,y_0,z_0)$, 法向量为$\mathbf{v}=(a,b,c)$ 的平面的方程
  $a(x-x_0)+b(y-y_0)+c(z-z_0)=0$