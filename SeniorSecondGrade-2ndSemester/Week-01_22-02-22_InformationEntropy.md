## 初遇信息熵 Information Entropy

- 2022-02-22

[toc]

### 引子问题

信息学之父*香农*定义随机变量 $X$ 的**信息熵** $H(X)={\displaystyle -\sum_{i=1}^{n} P(x_i)\log_2 P(x_i)}$ ，其中 $x_i$ 为基本事件，$n$ 为基本事件的个数，$P(x_i)$ 为基本事件 $x_i$ 的概率。例如「抛一次硬币」的*信息熵* $H(X)=-\left(\dfrac{1}{2}\log_2 \dfrac{1}{2}+\dfrac{1}{2}\log_2 \dfrac{1}{2}\right)=1$ 
(1) 若 $x+y=a\quad (x,\,y,\,a>0)$ ，证明：$x\log_2 x+y\log_2 y\ge a\log_2 \dfrac{a}{2}$ 
(2) 证明：$H(X)\le \log_2 n$ 

### 解答

(1)
设 $y=a-x,\,f(x)=x\log_2 x+y\log_2 y=x\log_2 x+(a-x)\log_2 (a-x)$ 

则 $f'(x)=\dfrac{1}{\ln 2}\left(\log_2x+1-\log_2(a-x)-1\right)=\dfrac{\log_2\left(\dfrac{x}{a-x}\right)}{\ln 2}$ 

分析知当 $x\in \left\lparen 0, \dfrac{a}{2}\right\rparen$ 时 $f(x)$ 单调递减，当 $x \in \left\lparen \dfrac{a}{2}, a\right\rparen$ 时 $f(x)$ 单调递增，故 $f(x)$ 在 $x=\dfrac{a}{2}$ 处取得最小值 $f_{\min }(x)=a\log_2 \dfrac{a}{2}$ 

(2)
不妨设 $p_i=P(x_i),\,p_1\le p_2\le \cdots \le p_n$ 

定义操作 $M$ 如下：

令 $x=\min (p_i),\,y=\max (p_i),\,p=\dfrac{1}{n}$ ，则 $x\le p\le y$ 

若 $p\ge \dfrac{x+y}{2}$ ，则 $p\le y$ ，由 (1) 知 $x\log_2x+y\log_2y\ge p\log_2p+(x+y-p)\log_2(x+y-p)$ 

若 $p\le \dfrac{x+y}{2}$ ，则 $p\ge x$ ，由 (1) 知 $x\log_2x+y\log_2y\ge p\log_2p+(x+y-p)\log_2(x+y-p)$ 

即 $x\log_2x+y\log_2y\ge p\log_2p+(x+y-p)\log_2(x+y-p)$ 

由于 ${\displaystyle \sum_{i=1}^{n}=1}$ 仍成立，因此上面的步骤可以一直进行。

而每次操作都会产生一个 $p\log_2p$ ，因此只需进行 $n-1$ 次操作就有所有 $p_i$ 都被替换为 $p$ 

即 $p_1\log_2p_1+p_2\log_2p_2+\cdots +p_n\log_2p_n={\displaystyle \sum_{i=1}^{n}p_i\log_2p_i\ge n\cdot p\log_2p=\log_2 \dfrac{1}{n}}$ 

即 $H(X)=-{\displaystyle \sum_{i=1}^{n}p_i\log_2p_i}\le -\log_2 \dfrac{1}{n}=\log_2n$ 

### 引理

> 若 ${\displaystyle \sum_{i=1}^{n}a_i=r;\;a_i,\,r> 0}$ ，则 ${\displaystyle \prod_{i=1}^{n}a_i^{a_i}=a_1^{a_1}a_2^{a_2}\cdots a_n^{a_n}\ge \left(\dfrac{r}{n}\right)^r}$ 

证明：
命题等价于证明 ${\displaystyle \sum_{i=1}^{n}a_i\ln a_i\ge r\ln \dfrac{r}{n}}$ 

令 $b_i=\dfrac{a_i}{r}$ ，则 ${\displaystyle \sum_{i=1}^{n}b_i}=1$ 

则 ${\displaystyle \sum_{i=1}^{n}a_i\ln a_i = r\left(\sum_{i=1}^{n}b_i\ln b_i + \ln r\sum_{i=1}^{n}b_i\right)\ge r\ln \dfrac{r}{n}}$ 

### 参考

> [知乎苗华栋的回答](https://www.zhihu.com/question/60227816/answer/1274071217)
> [信息熵最大值的证明](http://www.math345.com/blog/article/17)