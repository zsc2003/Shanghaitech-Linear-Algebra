---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial 
2023.12.5

---

# midterm review 期中复习
- 考试时间: 2023.12.6 星期三 8:15~9:55
- 考试地点: 教学中心202
- 考试内容: 第一章到第四章的4.8节（包含）
- 期中考试占总成绩 30%! 
-

# ppt中英文结合！！
作答中英文？？
试卷英文？ 不会的单词可以随时向助教提问


> 欢迎大家有问题随时在群里/私聊提问, 尽量不要拖延问题

---

# 一些要强调的事情
- **iff** $\Leftrightarrow$ if and only if $\Leftrightarrow$ 当且仅当, 
$\Rightarrow$ 充分性, $\Leftarrow$ 必要性, 都要证
或者全程使用$\Leftrightarrow$等价表述

free variables
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


---

# chapter 1
- 
- 
- 

---

# coeffcient matrix(系数矩阵) & 
# augmented matrix(增广矩阵)

![](./img/coeffcient_matrix.png) ![](./img/augmented_matrix.png)

系数矩阵 $A$ and 增广矩阵 $\bar{A}=(A|\mathbf{b})$

---

# 初等行变换
- 交换两行
- 用一个非零常数乘以某一行
- 用一个非零常数乘以某一行，然后加到另一行上

> 注意化简矩阵的时候的符号写法, 写出矩阵的化简方式

---

## row echelon form(行阶梯矩阵)
- leading 1(首1/主1/主元......)
- Any row in the matrix that is 0 must be below the row that is not 0
- upper row's leading 1 must be to the left of the lower row's leading 1

## reduced row echelon form(简化行阶梯矩阵)

- The leading 1 contained in any row of the matrix that is not 0 is the only term in the column that is not 0

---

# Gauss elimination
1. no solution
2. fixed solution
3. infinite solutions

---

# leading variable & free variable

$B$ is an augmented matrix of a linear system, its row echelon form is $\tilde{B}$

The unknowns corresponding to the leading 1 in the rows that are not 0 in $\tilde{B}$ are called the **leading variables** of the system of equations, and all the unknowns other than the leading variables are called the **free variables** of the system of equations.


















---

# chapter 2
-












---

# chapter 3

























---


# chapter 4


