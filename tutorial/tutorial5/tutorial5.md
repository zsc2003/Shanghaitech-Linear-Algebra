---
marp: true
math: mathjax
paginate: true

---

# Linear Algebra Tutorial5
2023.11.7

---

# homework

---

# homework

---

# Euclidean space

$\mathbb{R}^n$

---

# norm, distance

- normalization

---

# dot product

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
$balabala$




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

# cross product
求与两个向量正交的向量

点叉乘->所在直线？？？？？
直线->交点

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

---

# cross product geometric meaning

- parallelogram area
    平行四边形面积

- volume of parallelepiped
    平行六面体体积
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