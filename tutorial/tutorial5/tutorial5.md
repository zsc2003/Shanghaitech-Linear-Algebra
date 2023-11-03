---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial5
2023.11.7

---

# homework
- bonus
$A,B\in M_{3\times 3}$
$A^2-AB-2B^2=A-2BA-B$
$B=\begin{bmatrix}
-1 & 2 & 1 \\
0 & 1 & -1 \\
1 & 3 & 2
\end{bmatrix}$
$det(A-B)\neq 0$

---

---

# Cramer's rule

$A\mathbf{x}=\mathbf{b}$, $|A|\neq 0$ ($A_{n\times n}$)


$A=\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & & & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{bmatrix}$, $A_i=\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1,i-1} & b_1 & a_{1,i+1} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2,i-1} & b_2 & a_{2,i+1} & \cdots & a_{2n} \\
\vdots & & & & \vdots & & & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{n,i-1} & b_n & a_{n,i+1} & \cdots & a_{nn}
\end{bmatrix}$

then $x_i=\dfrac{|A_i|}{|A|}$

where $A_i$ is the matrix obtained from $A$ by replacing the $i$th column of $A$ by $\mathbf{b}$

---

# Cramer's rule

- e.g. when the coefficient is complicated
- **directly solve one of the variables**

![](./img/cramer.png)

---

# determinant property

![](./img/C.png)
![](./img/A.png) ![](./img/B.png)

> $|C| = |A| + |B|$

---

find $A=\left | \begin{matrix}
ax+by & ay+bz & az+bx \\
ay+bz & az+bx & ax+by \\
az+bx & ax+by & ay+bz  
\end{matrix} \right |$

---

# math review
- vector
- Cauchy inequality
- dot product
- cross product
$\vdots$

---

# Euclidean space

- $\mathbb{R}^n$ n-dimensional Euclidean space
  $\mathbf{v}\in\mathbb{R}^n$, $\mathbf{v}=(v_1,\cdots,v_n)$
- **linear combination**
  $\mathbf{w} = k_1\mathbf{v}_1 + k_2\mathbf{v}_2 + \cdots + k_r\mathbf{v}_r$
  $\mathbf{w}$ is the linear combination of $\mathbf{v}_1,\cdots,\mathbf{v}_r$
  $k_1,\cdots,k_r$ are the coefficients of $\mathbf{v}_1,\cdots,\mathbf{v}_r$
- **span**
    the set of all linear combinations of $\mathbf{v}_1,\cdots,\mathbf{v}_r$ is called the span of $\mathbf{v}_1,\cdots,\mathbf{v}_r$
    $span\{\mathbf{v}_1,\cdots,\mathbf{v}_r\}=\{\mathbf{w}|\mathbf{w}=k_1\mathbf{v}_1 + k_2\mathbf{v}_2 + \cdots + k_r\mathbf{v}_r, k_1,\cdots,k_r\in\mathbb{R}\}$
---

# linear independence*

- standard unit vector 标准单位向量
    there are $n$ standard unit vectors in $\mathbb{R}^n$
    $\mathbf{e}_i=(0,\cdots,0,1,0,\cdots,0)$
    $\mathbf{e}_i$ has 1 in the $i$-th position and 0 elsewhere
    eg. $\mathbf{w}=(1, 2)$, $\mathbf{w}=1\mathbf{e}_1+2\mathbf{e}_2$

- is the representation unique?
    $\mathbf{w}=(1,2)$
    $\mathbf{v_1}=(1, 0),\mathbf{v_2} = (0, 1),\mathbf{v_3} = (1, 1)$
    $\mathbf{w}=1\mathbf{v_1}+2\mathbf{v_2}+0\mathbf{v_3}$
    $\mathbf{w}=-1\mathbf{v_1}+0\mathbf{v_2}+1\mathbf{v_3}$
    $\mathbf{w}=0\mathbf{v_1}+1\mathbf{v_2}+1\mathbf{v_3}$
> unique represetation $\Leftrightarrow$ linearly independent
---

# linear independence*
- $\mathbf{v}_1,\cdots,\mathbf{v}_r$ are linearly independent if the only solution of $k_1\mathbf{v}_1 + k_2\mathbf{v}_2 + \cdots + k_r\mathbf{v}_r=\mathbf{0}$ is $k_1=k_2=\cdots=k_r=0$
- $\mathbf{v}_1,\cdots,\mathbf{v}_r$ are linearly dependent if and only if one of them is a linear combination of the others

---

# norm

- norm(Euclidean norm)
$\left\|\mathbf{v}\right\|=\sqrt{v_1^2+v_2^2+\cdots+v_n^2}$
    distance to the origin
    $\left\|\mathbf{v}\right\|\geq 0$
    $\left\|\mathbf{v}\right\|=0\Leftrightarrow \mathbf{v}=\mathbf{0}$
    $\left\|k\mathbf{v}\right\|=|k|\left\|\mathbf{v}\right\|$

- normalization
    $\mathbf{u}=\dfrac{\mathbf{v}}{\left\|\mathbf{v}\right\|}$
    get the unit vector $\mathbf{u}$: normailize $\mathbf{v}$

---

# distance
the Euclidean distance between $\mathbf{u}$ and $\mathbf{v}$
$d(u,v)=d(u,v)=\left\|\mathbf{u}-\mathbf{v}\right\|=\sqrt{(u_1-v_1)^2+(u_2-v_2)^2+\cdots+(u_n-v_n)^2}$

---

# dot(inner) product
- $\mathbf{u}\cdot\mathbf{w}=u_1w_1+u_2w_2+\cdots+u_nw_n$

So the Euclidean norm can be represented by the dot product
- $\left\|\mathbf{v}\right\|=\sqrt{\mathbf{v}\cdot\mathbf{v}}$

regard $\mathbf{v},\mathbf{w}$ as a column vector
$\mathbf{v}\cdot\mathbf{w}=\mathbf{w}\cdot\mathbf{v}=\mathbf{v}^T\mathbf{w}=\mathbf{w}^T\mathbf{v}$

if $A_{n\times n}$, $\mathbf{v},\mathbf{w}\in\mathbb{R}^n$

- $\mathbf{Av}\cdot\mathbf{w}=(\mathbf{Av})^T\mathbf{w}=\mathbf{v}^T\mathbf{A}^T\mathbf{w}=\mathbf{v}\cdot\mathbf{A}^T\mathbf{w}$
- $\mathbf{v}\cdot\mathbf{Aw}=\mathbf{v}^T(\mathbf{A}\mathbf{w})=(\mathbf{v}^T\mathbf{A})\mathbf{w}=(\mathbf{A}\mathbf{v}^T)^T\mathbf{w}=\mathbf{A}^T\mathbf{v}\cdot\mathbf{w}$

---

# Cauchy-Schwarz inequality
- vector version
 $|\mathbf{u}-\mathbf{v}|\leq\left\|\mathbf{u}\right\|+\left\|\mathbf{v}\right\|$
- calculus version
 $\int_a^b f(x)g(x)dx\leq\sqrt{\int_a^b f^2(x)dx}\sqrt{\int_a^b g^2(x)dx}$
- probability version
 $|E(XY)|\leq\sqrt{E(X^2)}\sqrt{E(Y^2)}$

---

# triangle inequality

- 












---

# angle
angle $\theta$ between two vectors $\mathbf{x},\mathbf{y}$ **$\leftarrow$ no zero vector**
$cos\theta = \dfrac{<\mathbf{x},\mathbf{y}>}{\sqrt{<\mathbf{x},\mathbf{x}>}\cdot\sqrt{<\mathbf{y},\mathbf{y}>}} = \dfrac{\mathbf{x}^T\mathbf{y}}{\left\|\mathbf{x}\right\|\left\|\mathbf{\mathbf{y}}\right\|}$

so $\mathbf{x}\cdot\mathbf{y}=\left\|\mathbf{x}\right\|\left\|\mathbf{\mathbf{y}}\right\|cos\theta$

$\mathbf{x}\cdot \mathbf{y}=0\Leftrightarrow \mathbf{x}\perp \mathbf{y}$

---

# Orthogonality

...

- orthogonal set
$\mathbf{v}_1,\cdots,\mathbf{v}_n$ are orthogonal
$\left\|\mathbf{v}_1+\cdots+\mathbf{v}_n\right\|= \left\|\mathbf{v}_1\right\|+\cdots+\left\|\mathbf{v}_n\right\|$
proof in hw




---

# Projection Theorem
- orthogonal projection of $\mathbf{u}$ on $\mathbf{v}$
$\mathbf{w}_1=proj_{\mathbf{v}}(\mathbf{u})=\dfrac{\mathbf{u}\cdot\mathbf{v}}{\left\|v\right\|^2}\mathbf{v}$

- the vector component of \mathbf{u} orthogonal to \mathbf{v}
$\mathbf{w}_2=\mathbf{u}-\mathbf{w}_1=\mathbf{u}-proj_{\mathbf{v}}(\mathbf{u})=\mathbf{u}-\dfrac{\mathbf{u}\cdot\mathbf{v}}{\left\|v\right\|^2}\mathbf{v}$


---
# cross product
![w:15cm](./img/cross1.png) ![w:14cm](./img/cross2.png) 


---

# cross product
$\mathbf{x}\times\mathbf{y}=\begin{bmatrix}
x_2y_3-x_3y_2 \\
x_3y_1-x_1y_3 \\
x_1y_2-x_2y_1
\end{bmatrix}$
- $\mathbf{x}\times\mathbf{y}$ is orthogonal to both $\mathbf{x}$ and $\mathbf{y}$
- $\left\|\mathbf{x}\times\mathbf{y}\right\|=\left\|\mathbf{x}\right\|\left\|\mathbf{y}\right\|sin\theta$
- $\mathbf{x}\times\mathbf{y}=-\mathbf{y}\times\mathbf{x}$
- $\mathbf{x}\times(\mathbf{y}+\mathbf{z})=\mathbf{x}\times\mathbf{y}+\mathbf{x}\times\mathbf{z}$
- $(k\mathbf{x})\times\mathbf{y}=k(\mathbf{x}\times\mathbf{y})$

---

# cross product
- the cross product of two vectors can be represented by the determinant
$\mathbf{x}\times\mathbf{y}=\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
x_1 & x_2 & x_3 \\
y_1 & y_2 & y_3
\end{vmatrix}$
- $\mathbf{x}\times\mathbf{y}=\mathbf{0}\Leftrightarrow \mathbf{x}\parallel\mathbf{y}$

- we can also transfer $\mathbf{x}$ into a matrix $[\mathbf{x}]\mathbf{y}$
where $[\mathbf{x}]=\begin{bmatrix}
0 & -x_3 & x_2 \\
x_3 & 0 & -x_1 \\
-x_2 & x_1 & 0
\end{bmatrix}$

> notice that $[\mathbf{x}]$ is skew-symmetric, so its rank is odd
actually, rank($[\mathbf{x}]$)=2

---

# scalar triple product
- 标量三重积(混合积)
$\mathbf{x}\cdot(\mathbf{y}\times\mathbf{z})=\begin{vmatrix}
x_1 & x_2 & x_3 \\
y_1 & y_2 & y_3 \\
z_1 & z_2 & z_3
\end{vmatrix}$
- $\mathbf{x}\cdot(\mathbf{y}\times\mathbf{z})=\mathbf{y}\cdot(\mathbf{z}\times\mathbf{x})=\mathbf{z}\cdot(\mathbf{x}\times\mathbf{y})$
- $\mathbf{x}\cdot(\mathbf{y}\times\mathbf{z})=\mathbf{0}\Leftrightarrow \mathbf{x},\mathbf{y},\mathbf{z}$ are coplanar
- $\mathbf{x}\cdot(\mathbf{y}\times\mathbf{z})=\left\|\mathbf{x}\right\|\left\|\mathbf{y}\times\mathbf{z}\right\|cos\theta$
- $\mathbf{x}\cdot(\mathbf{y}\times\mathbf{z})=\left\|\mathbf{y}\right\|\left\|\mathbf{z}\times\mathbf{x}\right\|cos\theta$
- $\mathbf{x}\cdot(\mathbf{y}\times\mathbf{z})=\left\|\mathbf{z}\right\|\left\|\mathbf{x}\times\mathbf{y}\right\|cos\theta$

- Lagrange’s identity
$\left\|\mathbf{u}\times\mathbf{v}\right\|^2=\left\|\mathbf{u}\right\|^2\left\|\mathbf{v}\right\|^2-(\mathbf{u}\cdot\mathbf{v})^2$


---

# cross product geometric meaning

- parallelogram area
    平行四边形面积

- volume of parallelepiped
    平行六面体体积
---

# exercise (21-mid)

![](./img/mid1.png)

---

# exercise (20-mid)

![](./img/mid2.png)

---


# representation of lines and planes
- line
$\mathbf{r}=\mathbf{r}_0+t\mathbf{v}$
$\dfrac{x-x_0}{v_1}=\dfrac{y-y_0}{v_2}=\dfrac{z-z_0}{v_3}$
$\mathbf{v}=(v_1,v_2,v_3)$ is the direction vector of the line

- plane
$\mathbf{r}=\mathbf{r}_0+s\mathbf{v}+t\mathbf{w}$
$n_1(x-x_0)+n_2(y-y_0)+n_3(z-z_0)=0$
$\mathbf{n}=(n_1,n_2,n_3)$ is the normal vector of the plane
$\mathbf{n}= \mathbf{v}\times\mathbf{w}$


---

# cross product

过平面上两点$p_1=(x_1,y_1)$,$p_2=(x_2,y_2)的

齐次坐标: $p_1=(x_1,y_1,1)$,$p_2=(x_2,y_2,1)$
直线的方向向量: $\mathbf{v}=\mathbf{p}_1\times\mathbf{p}_2$

两条直线: $\mathbf{v}_1,\mathbf{v}_2$
交点: $\mathbf{p}=\mathbf{v}_1\times\mathbf{v}_2$

前提: 平面上