---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial 1
2023.10.??

---

# self introduction

- 周守琛
- 2021 cs undergraduate
- qq: 1354038619
- email: zhoushch@shanghaitech.edu.cn
---

# About the tutorial
- time: Every :00
- place: SIST 1-??? 

1. hand out homework
  grade distribution:
  平时成绩 30%； 期中考试30%；期末考试 40%
2. some discussion(please post your questions before the tutorial)
3. why in English?

---

# About academic integrity

- No Plagiarism
- No Plagiarism
- No Plagiarism

着重强调学术诚信问题, 禁止抄袭!
鼓励讨论交流
feel free to contact TAs

---

# Why Linear Algebra?

- Linear algebra is the study of vectors and linear transformations.
- It is a fundamental mathematical subject with applications in many fields.
- It is a prerequisite for many other courses.
- ...

---

# What is Linear
- linearity = additivity + homogeneity

1. additivity
  f(x+y) = f(x) + f(y)
2. homogeneity
  f(ax) = af(x)

- more properties will be introduced later(chapter 4  Linear Spaces)

- In this cource, we will mostly focus on linear spaces and linear transformations.

---

# Linear equation(s)
![linear system](./img/linear_system.png)

---
# coeffcient matrix & augmented matrix
![](./img/coeffcient_matrix.png) ![](./img/augmented_matrix.png)


- specific: $\vec{b} = \vec{0}$:
called **homogeneous linear system**
  1. at least a **trivial solution**
  2. may have non-trivial solutions(linear independence) 

---

# some possible solutions
1. no solution
2. fixed solution
3. infinite solutions

- specific
  trivial solution: $\vec{x} = \vec{0}$





---
general solution
specific solution + trivial solution

Ax=b
通解可由一个特解加上齐次方程的通解得到

---
# elementary row operations
- interchange two rows
- multiply a row by a nonzero constant
- add a multiple of one row to another row





---

# Some useful resources

- 3B1B Essence of Linear Algebra
  直接在B站搜 3b1b线性代数的本质 即可

---

trival solution