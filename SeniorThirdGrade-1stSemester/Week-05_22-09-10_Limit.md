## 极限初探

> 下面使用标准的**极限**定义：\(\varepsilon-\delta\) 语言
>
> \(\forall_{\varepsilon > 0},\exist_{\delta > 0},\forall_{\left\vert x-a\right\vert < \delta},|f(x) - L| < \varepsilon \iff \lim\limits_{x \to a}f(x)=L\) 

### 引语

知道极限许久，却一直记不住准确定义。前几天从残存的记忆中拼凑出来了（虽然两个符号用反了），因此借此巩固对极限的理解。

根据定义出发，本文将要证明三个定理

1. 常：\(\lim\limits_{x \to a}kf(x) = k\lim\limits_{x \to a}f(x)\) 
2. 和：\(\lim\limits_{x \to a}\left[f(x) + g(x)\right] = \lim\limits_{x \to a}f(x) + \lim\limits_{x \to a}g(x)\) 
3. 积：\(\lim\limits_{x \to a}\left[f(x)\cdot g(x)\right] = \lim\limits_{x \to a}f(x)\cdot \lim\limits_{x \to a}g(x)\) 

此外，为简化问题，定义 \(\lim\limits_{x \to a}f(x)=F,\,\lim\limits_{x \to a}g(x)=G\)，且 \(F,G \in \R\)

### 常 1

\(k=0\) 显然成立，因此先证明 \(k > 0\) 的情形

\[
\lim\limits_{x \to a}f(x)=F \iff \forall_{\varepsilon>0},\exist_{\delta>0},\forall_{|x-a|<\delta},|f(x) - F| < \varepsilon
\]

那么有 \(|kf(x) - kF| < k \varepsilon\) 

当 \(k\le 1\) 时，有 \(k \varepsilon \le \varepsilon\)

那么有

\[
\forall_{\varepsilon>0},\exist_{\delta>0},\forall_{|x-a|<\delta},|kf(x) - kF| < \varepsilon
\]

也即 \(\lim\limits_{x \to a}kf(x)=kF=k \lim\limits_{x \to a}f(x)\)

### 和

\[
\lim\limits_{x \to a}f(x)=F \iff \forall_{\varepsilon>0},\exist_{\delta_1>0},\forall_{|x-a|<\delta_1},|f(x) - F| < \varepsilon\\
\lim\limits_{x \to a}g(x)=G \iff \forall_{\varepsilon>0},\exist_{\delta_2>0},\forall_{|x-a|<\delta_2},|g(x) - G| < \varepsilon
\]

取 \(\delta = \min\{\delta_1,\,\delta_2\}\)

那么

\[
\forall_{\varepsilon>0},\exist_{\delta>0},\forall_{|x-a|<\delta},\\
\begin{aligned}
    |f(x) - F| < \varepsilon,\,|g(x) - G| < \varepsilon &\iff F - \varepsilon < f(x) < F + \varepsilon,\,G-\varepsilon < g(x) < G + \varepsilon\\
    &\iff F + G - 2 \varepsilon < f(x) + g(x) < F + G + 2 \varepsilon\\
    &\iff \left\vert \dfrac{f(x) + g(x)}{2} - \dfrac{F + G}{2}\right\vert < \varepsilon\\
    &\iff \lim\limits_{x \to a}\left[ \dfrac{f(x) + g(x)}{2}\right ] = \dfrac{F + G}{2}\\
    &\iff \dfrac{1}{2}\lim\limits_{x \to a}[f(x) + g(x)] = \dfrac{F + G}{2}\\
    &\iff \lim\limits_{x \to a}[f(x) + g(x)] = \lim\limits_{x \to a}f(x) + \lim\limits_{x \to a}g(x)
\end{aligned}
\]

### 常 2

\(k > 1\) 时，记 \(\displaystyle \sum_{i=1}^{n}k_i=k,\,\forall_{i},0<k_i\le 1\) 

那么

\[
\begin{aligned}
    \lim\limits_{x \to a}kf(x) &= \lim\limits_{x \to a}\left[\sum_{i=1}^{n}k_if(x)\right]\\
    &=\sum_{i=1}^{n}\left[ \lim\limits_{x \to a}k_if(x)\right ]\\
    &=\sum_{i=1}^{n}\left[k_i \lim\limits_{x \to a}f(x)\right]\\
    &=\sum_{i=1}^{n}k_iF\\
    &=kF\\
    &=k \lim\limits_{x \to a}f(x)
\end{aligned}
\]

\(k< 0\) 情况同理，此处证明略。（稿纸有写，但我没时间敲了）

### 积

先证明一种简单情形，即 \(F=G=0\) 

则

\[
\forall_{\varepsilon>0},\exist_{\delta>0},\forall_{|x-a|<\delta},|f(x)| < \varepsilon,\,|g(x)| < \varepsilon \iff |f(x)\cdot g(x)| < \varepsilon^2
\]

\(\varepsilon \le 1\) 时有 \(|f(x)\cdot g(x)| < \varepsilon^2 \le \varepsilon\)，记此时的 \(\delta=\Delta(\varepsilon)\)，\(\varepsilon > 1\) 时取 \(\delta = \Delta(1)\)，则有 \(|f(x)\cdot g(x)| < 1 < \varepsilon\) 也成立

因此

\[
\lim\limits_{x \to a}\left[f(x)\cdot g(x)\right]=0
\]

那么

\[
\begin{aligned}
    \lim\limits_{x \to a}\left[f(x)\cdot g(x)\right] &= \lim\limits_{x \to a}\left[\left( f(x) - F\right )\left( g(x) - G\right )\right] + F \lim\limits_{x \to a}g(x) + G \lim\limits_{x \to a}f(x) - FG\\
    &=0 + FG + FG -FG\\
    &=FG\\
    &=\lim\limits_{x \to a}f(x)\cdot \lim\limits_{x \to a}g(x)
\end{aligned}
\]
