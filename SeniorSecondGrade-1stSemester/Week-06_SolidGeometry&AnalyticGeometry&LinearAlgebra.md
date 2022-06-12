## 线性代数简化立体几何&解析几何运算

- 2021-10-09
- 编写时间：10-09, 10-10

[toc]

- [x] $\Anki$ （未拓展）

### 矩阵

由 $m\times n$ 个数 $a_{ij}$ 排成的 $m$ 行 $n$ 列的数称为 **$m$ 行 $n$ 列的矩阵**，简称 **$m\times n$ 矩阵**，记作
$$
\bm{A}=\begin{bmatrix}	a_{11} & a_{12} & \cdots  & a_{1n} \\ 	a_{21} & a_{22} & \cdots  & a_{2n} \\ 	\vdots  & \vdots  & \ddots  & \vdots  \\ 	a_{m1} & a_{m2} & \cdots  & a_{mn} \\ \end{bmatrix}
$$

这 $m\times n$ 个数称为矩阵 $\bm{A}$ 的**元素**，简称为**元**。数 $a_{ij}$ 位于矩阵 $\bm{A}$ 的第 $i$ 行第 $j$ 列，称为矩阵 $\bm{A}$ 的 $(\:\!i\,,\, j\:\!)$ 元，以数 $a_{ij}$ 为 $(\:\!i\,,\, j\:\!)$ 元的矩阵可记为 $(a_{ij})$ 或 $(a_{ij})_{m\times n}$ 。$m\times n$ 矩阵 $\bm{A}$ 也记作 $\bm{A}_{m\times n}$ 。

### 行列式

**行列式**是一个函数，定义域为矩阵 $\bm{A}$ ，取值为一个标量，记作 $\det (\bm{A})$ 或 $|\bm{A}|$ 。

对矩阵 $\bm{A}$ ：
$$
\bm{A}=\begin{bmatrix}	a_{11} & a_{12} & \cdots  & a_{1n} \\ 	a_{21} & a_{22} & \cdots  & a_{2n} \\ 	\vdots  & \vdots  & \ddots  & \vdots  \\ 	a_{m1} & a_{m2} & \cdots  & a_{mn} \\ \end{bmatrix}
$$

有
$$
\det (\bm{A})=\begin{vmatrix}	a_{11} & a_{12} & \cdots  & a_{1n} \\ 	a_{21} & a_{22} & \cdots  & a_{2n} \\ 	\vdots  & \vdots  & \ddots  & \vdots  \\ 	a_{m1} & a_{m2} & \cdots  & a_{mn} \\ \end{vmatrix}
$$

#### 二阶行列式

讨论一个二元线性方程组：
$$
\env{cases}{a_1x+b_1y=c_1\\a_2x+b_2y=c_2}
$$

记
$$
D=\begin{vmatrix}	a_1 & b_1 \\ 	a_2 & b_2 \\ \end{vmatrix}=a_1b_2-a_2b_1
$$
为**二阶行列式**。

令
$$
D_1=\begin{vmatrix}	c_1 & b_1 \\ 	c_2 & b_2 \\ \end{vmatrix}
$$

$$
D_2=\begin{vmatrix}	a_1 & c_1 \\ 	a_2 & c_2 \\ \end{vmatrix}
$$

则
$$
\env{cases}{x=\dfrac{D_1}{D}\\y=\dfrac{D_2}{D}}
$$

当且仅当 $D\ne 0$ 时成立。

当 $D=0$ 时方程可能无解，也可能有无数多组解。

#### 三阶行列式

讨论一个三元线性方程组：
$$
\env{cases}{a_1x+b_1y+c_1z=d_1\\a_2x+b_2y+c_2z=d_2\\a_3x+b_3y+c_3z=d_3}
$$

记
$$
D=\begin{vmatrix}	a_1 & b_1 & c_1 \\ 	a_2 & b_2 & c_2 \\ 	a_3 & b_3 & c_3 \\ \end{vmatrix}=a_1b_2c_3+a_3b_1c_2+a_2b_3c_1-a_3b_2c_1-a_2b_1c_3-a_1b_3c_2
$$
为**三阶行列式**。

三阶行列式**对角线法则**：
$$
\begin{vmatrix}	a_1 & b_1 & c_1 \\ 	a_2 & b_2 & c_2 \\ 	a_3 & b_3 & c_3 \\ \end{vmatrix}=a_1b_2c_3+b_1c_2a_3+c_1a_2b_3-c_1b_2a_3-b_1a_2c_3-a_1c_2b_3
$$

注：对角线法则仅适用于二阶、三阶行列式。

令
$$
D_1=\begin{vmatrix}	d_1 & b_1 & c_1 \\ 	d_2 & b_2 & c_2 \\ 	d_3 & b_3 & c_3 \\ \end{vmatrix}
$$

$$
D_2=\begin{vmatrix}	a_1 & d_1 & c_1 \\ 	a_2 & d_2 & c_2 \\ 	a_3 & d_3 & c_3 \\ \end{vmatrix}
$$

$$
D_3=\begin{vmatrix}	a_1 & b_1 & d_1 \\ 	a_2 & b_2 & d_2 \\ 	a_3 & b_3 & d_3 \\ \end{vmatrix}
$$

则
$$
\env{cases}{x=\dfrac{D_1}{D}\\y=\dfrac{D_2}{D}\\z=\dfrac{D_3}{D}}
$$

当且仅当 $D\ne 0$ 时成立。

当 $D=0$ 时方程可能无解，也可能有无数多组解。

### 向量叉乘

记
$$
\left|\bm{u}\boldsymbol{\times}\bm{v}\right|=|\bm{u}||\bm{v}|\sin \lang\bm{u},\bm{v}\rang
$$
为向量 $\bm{u}$ 与 $\bm{v}$ **叉乘**的模。

$(\bm{u}\boldsymbol{\times}\bm{v})\perp \bm{u},\bm{v}$ 

右手拇指指向 $\bm{u}$ ，右手食指指向 $\bm{v}$ ，自然伸出中指的方向就是 $\bm{u}\boldsymbol{\times}\bm{v}$ 的方向。

当 $\bm{u},\bm{v}$ 至少有一个为 $\bm{0}$ 时，定义 $\bm{u}\boldsymbol{\times}\bm{v}=\bm{0}$ 。当非零向量 $\bm{u}\par \bm{v}$ 时，$\bm{u}\boldsymbol{\times}\bm{v}=\bm{0}$ 。

#### 叉乘的性质

##### 运算律

1. $(m \bm{u})\boldsymbol{\times}(n \bm{v})=(mn)(\bm{u}\boldsymbol{\times}\bm{v})$ 
2. $\bm{u}\boldsymbol{\times}(\bm{v}+\bm{w})=\bm{u}\boldsymbol{\times}\bm{v}+\bm{u}\boldsymbol{\times}\bm{w}$ 
3. $(\bm{v}+\bm{w})\boldsymbol{\times}\bm{u}=\bm{v}\boldsymbol{\times}\bm{u}+\bm{w}\boldsymbol{\times}\bm{u}$ 
4. $\bm{v}\boldsymbol{\times}\bm{u}=-(\bm{u}\boldsymbol{\times}\bm{v})$ 
5. $\bm{0}\boldsymbol{\times}\bm{u}=\bm{0}$ 

##### 几何性质

$\left|\bm{u}\boldsymbol{\times}\bm{v}\right|$ 是 $\bm{u}$ 和 $\bm{v}$ 确定的平行四边形的面积。

##### 行列式表示

若
$$
\env{aligned}{\bm{u}&=a_1 \bm{i}+b_1 \bm{j}+c_1 \bm{k}\\\bm{v}&=a_2 \bm{i}+b_2 \bm{j}+c_2 \bm{k}}
$$

则
$$
\bm{u}\boldsymbol{\times}\bm{v}=\begin{vmatrix}	\bm{i} & \bm{j} & \bm{k} \\ 	a_1 & b_1 & c_1 \\ 	a_2 & b_2 & c_2 \\ \end{vmatrix}
$$

##### 法向量

对于某平面 $\alpha$ 上两条不共线的向量 $\bm{u},\bm{v}$ ，有平面 $\alpha$ 的法向量之一 $\bm{n}_{\alpha}=\bm{u}\boldsymbol{\times}\bm{v}$ 。

对于
$$
\env{aligned}{\bm{u}&=(\:\!a_1\,,\, b_1\,,\, c_1\:\!)\\ \bm{v}&=(\:\!a_2\,,\, b_2\,,\, c_2\:\!)}
$$

有
$$
\env{aligned}{\bm{u}\boldsymbol{\times}\bm{v}&=\left(\:\!\begin{vmatrix}	b_1 & c_1 \\ 	b_2 & c_2 \\ \end{vmatrix}\,,\, -\begin{vmatrix}	a_1 & c_1 \\ 	a_2 & c_2 \\ \end{vmatrix}\,,\, \begin{vmatrix}	a_1 & b_1 \\ 	a_2 & b_2 \\ \end{vmatrix}\:\!\right)\\&=\left(\:\!b_1c_2-b_2c_1\,,\, a_2c_1-a_1c_2\,,\, a_1b_2-a_2b_1\:\!\right)}
$$

求两平面 $\alpha,\beta$ 的二面角 $\theta$ 的余弦值时，求出两法向量 $\bm{n}_{\alpha},\bm{n}_{\beta}$ 并在图上标注方向。

若两法向量的方向均指向二面角内部，或均指向二面角外部，则 $\cos \theta=-\dfrac{\bm{n}_{\alpha}\boldsymbol{\cdot}\bm{n}_{\beta}}{\left|\bm{n}_{\alpha}\right|\left|\bm{n}_{\beta}\right|}$ 

若两法向量的方向一个指向二面角内部，一个指向二面角外部，则 $\cos \theta=\dfrac{\bm{n}_{\alpha}\boldsymbol{\cdot}\bm{n}_{\beta}}{\left|\bm{n}_{\alpha}\right|\left|\bm{n}_{\beta}\right|}$ 

### 向量混合积（拓展）

积 $(\bm{u}\boldsymbol{\times}\bm{v})\boldsymbol{\cdot}\bm{w}$ 称为 $\bm{u},\bm{v},\bm{w}$ 的**混合积**。记作 $[\bm{u}\;\bm{v}\;\bm{w}]$ 。即
$$
[\bm{u}\;\bm{v}\;\bm{w}]=|\bm{u}\boldsymbol{\times}\bm{v}||\bm{w}|\cos \lang\bm{u}\boldsymbol{\times}\bm{v},\bm{w}\rang
$$

$\big|[\bm{u}\;\bm{v}\;\bm{w}]\big|$ 的几何意义是 $\bm{u},\bm{v},\bm{w}$ 确定的平行六面体的体积。

#### 性质

##### 运算律

1. $[\bm{u}\;\bm{v}\;\bm{w}]=[\bm{v}\;\bm{w}\;\bm{u}]=[\bm{w}\;\bm{u}\;\bm{v}]$ 
2. $(\bm{u}\boldsymbol{\times}\bm{v})\boldsymbol{\cdot}\bm{w}=\bm{u}\boldsymbol{\cdot}(\bm{v}\boldsymbol{\times}\bm{w})$ 
3. $[\bm{u}\;\bm{v}\;(\lambda \bm{t}+\mu \bm{w})]=\lambda[\bm{u}\;\bm{v}\;\bm{t}]+\mu[\bm{u}\;\bm{v}\;\bm{w}]$ 

##### 行列式表示

若
$$
\env{aligned}{\bm{u}&=a_1 \bm{i}+b_1 \bm{j}+c_1 \bm{k}\\\bm{v}&=a_2 \bm{i}+b_2 \bm{j}+c_2 \bm{k}\\\bm{w}&=a_3 \bm{i}+b_3 \bm{j}+c_3 \bm{k}}
$$

则
$$
[\bm{u}\;\bm{v}\;\bm{w}]=(\bm{u}\boldsymbol{\times}\bm{v})\boldsymbol{\cdot}\bm{w}=\begin{vmatrix}	a_1 & b_1 & c_1 \\ 	a_2 & b_2 & c_2 \\ 	a_3 & b_3 & c_3 \\ \end{vmatrix}
$$