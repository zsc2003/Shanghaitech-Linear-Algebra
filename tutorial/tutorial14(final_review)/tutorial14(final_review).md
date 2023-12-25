---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial 14
2024.1.9

---

# final review 期末复习
- 考试时间: 2024.1. 星期 ~
- 考试地点: 教学中心
- 考试范围: 
- 期末考试占总成绩 30%
- 试卷为全英文, 不涉及数学的问题可以找监考人员翻译
- 作答中英文均可

---

# 一些要强调的事情
- 矩阵变换要从右往左看
    $T(\mathbf{x})=(T_3(T_2(T_1(\mathbf{x}))))=(T_3\circ T_2\circ T_1)(\mathbf{x})$
    $[T]=[T_3][T_2][T_1]$
- $T: \mathbb{R}^n\to \mathbb{R}^m$
    $[T]\in M_{m\times n}$
    $\mathbf{y}=T(\mathbf{x})=[T]\mathbf{x},\mathbf{x}\in \mathbb{R}^n,\mathbf{y}\in \mathbb{R}^m$
    所以在使用rank-nullity theorem时, 注意是$rank([T])+nullity([T])=n$


- $T:V\to W$, $W$ 为$T$的到达域(codomain),而不是值域(range)
    > $T$的值域(range)是$W$的子集

---
# review list 复习清单
- chapter4,5 向量空间(英文教材chapter 4)&线性变换(英文教材chapter 8)
    - 矩阵变换
    - 2
    - 3
- chapter6 特征值与特征向量(英文教材chapter 5)
    - 特征值与特征向量
    - 相似对角化
- chapter7

---

# chapter4,5 向量空间,线性变换
- 矩阵变换
- 2
- 3


---

## 线性变换(linear transformation)
- 定义域 domain
- 到达域/陪域 codomain
- 值域 range
- 线性变换 linear transformation
    - additivity 可加性
        $T(\mathbf{x}+\mathbf{y})=T(\mathbf{x})+T(\mathbf{y})$
    - homogeneity 齐次性
        $T(k\mathbf{x})=kT(\mathbf{x})$

---

## 线性变换(linear transformation)
$T:V\to W$
- 一一映射/单射 one-to-one/injective
    $T(\mathbf{x})=T(\mathbf{y})\Rightarrow \mathbf{x}=\mathbf{y}$
    $Ker(T)=\{\mathbf{0}\}$
    只有一一映射才存在逆映射(反函数)
- 满射 surjective/onto
    $R(T)=W$
    $\dim(R(T))=\dim(W)$
- 双射 bijective
    bijective = injective + surjective

---

## 线性变换与向量空间的关系
- $T:V\to W$



---

- 如果 $\dim(V) > \dim(W)$,那么$T$必然不可能是一一映射.
- 如果 $\dim(V) < \dim(W)$,那么$T$必然不可能是满射.

---

$T:V\to W$ is linear transformation

- Kernel
  $Ker(T): \{v\in V|T(v) = 0\}$
  $Ker(T)\subseteq V$ is a subspace of $V$
  $Ker(T)\Leftrightarrow Null([T])$

- range
  $RAN(T) / R(T): \{w\in W|w = T(v), v\in V\}$
  $R(T) \subseteq W$ is a subspace of $W$
  $R(T) \Leftrightarrow Col([T])$

- $\dim(Ker(T)) + \dim(R(T)) = \dim(V)$


---

# chapter6 特征值与特征向量(英文教材chapter 5)
- 特征值与特征向量
- 相似对角化

---

## 特征值与特征向量

---

## 相似对角化

---


