## 截距式方程相关结论与推导过程

- 2021-09-24

1. 如图，已知直线 $l:\:\dfrac{x}{a}+\dfrac{y}{b}=1\quad(\:\!a\,,\,b>0\:\!)$ 过定点 $P(\:\!m\,,\, n\:\!)$ ，其中 $m,\,n>0$ ，交 $x$ 轴于 $A(\:\!a\,,\, 0\:\!)$ ，交 $y$ 轴于 $B(\:\!0\,,\, b\:\!)$ 。求下列值的最小值：
   1. $OA+OB$ 
   2. $S_{\triangle OAB}$ 
   3. $PA\cdot PB$ 
   4. $AB$ 
   5. $C_{\triangle OAB}$ 

![](images/InterceptFormRelated.png)

由题意得 $\dfrac{m}{a}+\dfrac{n}{b}=1\Leftrightarrow an+bm=ab$ 

1. $OA+OB$ 

注意到

$$
\env{aligned}{a+b&=(a+b) \left(\dfrac{m}{a}+\dfrac{n}{b}\right)\\&=m+n+\dfrac{a}{b}n+\dfrac{b}{a}m\\&\ge m+n+2\sqrt{mn}}
$$

当 $\dfrac{a}{b}=\sqrt{\dfrac{m}{n}}$ 时取得等号

此时 $\env{cases}{a=m+\sqrt{mn}\\b=n+\sqrt{mn}}$ 

即 $(OA+OB)_{\min }=(a+b)_{\min }=m+n+2\sqrt{mn}$ 

2. $S_{\triangle OAB}$ 

注意到

$$
\env{aligned}{ab&=ab\left(\dfrac{m}{a}+\dfrac{n}{b}\right) \left(\dfrac{m}{a}+\dfrac{n}{b}\right)\\&=2mn+\dfrac{b}{a}m^2+\dfrac{a}{b}n^2\\&\ge 4mn}
$$

当 $\dfrac{a}{b}=\dfrac{m}{n}$ 时取得等号

此时 $\env{cases}{a=2m\\b=2n}$ 

即 $(S_{\triangle OAB})_{\min }=\dfrac{1}{2}ab=2mn$ 

3. $PA\cdot PB$ 

注意到

$$\env{aligned}{PA\cdot PB&=\sqrt{\left[m^2+(b-n)^2\right]\left[n^2+(a-m)^2\right]}\\&\ge \sqrt{[mn+(b-n)(a-m)]^2}\\&=2mn}$$

当 $a=b$ 时取得等号

此时 $\env{cases}{a=m+n\\b=m+n}$ 

即 $\left(PA\cdot PB\right)_{\min }=2mn$ 

4. $AB$ 

注意到

$$
\env{aligned}{a^2+b^2&=(a^2+b^2) \left(\dfrac{m}{a}+\dfrac{n}{b}\right) \left(\dfrac{m}{a}+\dfrac{n}{b}\right)\\&\ge (m^{\frac{2}{3}}+n^{\frac{2}{3}})^3}
$$

当 $\dfrac{a}{b}=\sqrt[3]{\dfrac{m}{n}}$ 时取得等号

此时 $\env{cases}{a=m+\sqrt[3]{mn^2}\\b=n+\sqrt[3]{m^2n}}$ 

即 $AB_{\min }=\left(\sqrt{a^2+b^2}\right)_{\min }=(m^{\frac{2}{3}}+n^{\frac{2}{3}})^{\frac{3}{2}}$


5. $C_{\triangle OAB}$ 

设 $t=\dfrac{a}{b}$ ，由题意知 $b=n+\dfrac{m}{t}$ 

注意到

$$
\env{aligned}{C(t)&=a+b+\sqrt{a^2+b^2}\\&=b\left(\dfrac{a}{b}+1+\sqrt{\dfrac{a^2}{b^2}+1}\right)\\&=\left(n+\dfrac{m}{t}\right)\left(t+1+\sqrt{t^2+1}\right)}
$$

则

$$
\env{aligned}{C^\prime(t)&=\dfrac{n t}{\sqrt{t^{2} + 1}}+n-\dfrac{m}{t^{2}}-\dfrac{m}{t^{2}\sqrt{t^{2} + 1}}\\&=\dfrac{1}{t^2\sqrt{t^2+1}}\left(nt^3+nt^2\sqrt{t^2+1}-m-m\sqrt{t^2+1}\right)}
$$

令 $C^\prime(t)=0$ ，则 $nt^3+nt^2\sqrt{t^2+1}-m-m\sqrt{t^2+1}=0$ 

整理得 $nt^2\left(\displaystyle\sqrt{t^2+1}+t\right)=m\left(\displaystyle\sqrt{t^2+1}+1\right)$ 

设 $t=\tan \theta\quad\left(\theta\in (\:\!0\,,\, \dfrac{\pi}{2}\:\!)\right)$ 

则

$$
\env{aligned}{\text{原式}&\Leftrightarrow n\tan ^2\theta(\tan \theta+\sec \theta)=m(\sec \theta+1)\\&\Leftrightarrow  \dfrac{n\sin ^3\theta}{\cos ^3\theta}+\dfrac{n\sin ^2\theta}{\cos ^3\theta}=\dfrac{m}{\cos \theta}+m\\&\Leftrightarrow n\sin ^2\theta\left(\sin \theta+1\right)=m\cos ^2\theta\left(\cos \theta+1\right)\\&\Leftrightarrow \dfrac{m}{n}=\tan ^2\theta \dfrac{\sin \theta+1}{\cos \theta+1}\\&\Leftrightarrow \dfrac{m}{n}=\tan ^2\theta \dfrac{2\sin \varphi \cos \varphi +\sin ^2\varphi+\cos ^2\varphi}{2\cos ^2\varphi}\\&\Leftrightarrow \dfrac{m}{n}=\tan ^2\theta \dfrac{2\tan \varphi+\tan ^2\varphi+1}{2}\\&\Leftrightarrow \sqrt{\dfrac{2m}{n}}= \tan\theta\left(\tan \varphi+1\right)\\&\Leftrightarrow a=\sqrt{t^2+1}+t-1\\&\Leftrightarrow t=\dfrac{a^2+2a}{2a+2}\\&\Leftrightarrow t=\dfrac{m+\sqrt{2mn}}{n+\sqrt{2mn}}}
$$

易见原式有最小值

则当 $\dfrac{a}{b}=\dfrac{m+\sqrt{2mn}}{n+\sqrt{2mn}}$ 时取得最小值

此时 $\env{cases}{a=\dfrac{\sqrt{2mn}\left(m+n+\sqrt{2mn}\right)}{n+\sqrt{2mn}}\\b=\dfrac{\sqrt{2mn}\left(m+n+\sqrt{2mn}\right)}{m+\sqrt{2mn}}}$ 

重新代回去很难算，我就用软件算了，结果长下面这样，复杂无比，但软件说是最简的：

$\left(C_{\triangle OAB}\right)_{\min }=\left(\sqrt{2m n}+m+n\right) \left(\dfrac{2m}{\sqrt{2m n}+2 m}+\dfrac{2n}{\sqrt{2m n}+2 n}+\sqrt{2m n \left[\dfrac{1}{\left(\sqrt{2mn}+m\right)^2}+\dfrac{1}{\left(\sqrt{2mn}+n\right)^2}\right]}\right)$

把 $\env{cases}{m=1\\n=1}$ 代入得 $C_{\min }=4+2\sqrt{2}$ ，是正确的。

把 $\env{cases}{m=3\\n=4}$ 代入得 $C_{\min }=14+4\sqrt{6}\approx 23.7979589711327$ 

此时 $a=9-\sqrt{6}\approx 6.550510257216822$ 

![](images/2021-09-24-22-05-10.png)

不是很明显，但我有理由相信它是在最低点。

就这样，Over

---

2021-10-07 更新：

经过尝试，将原式化简为

$$
\left(C_{\triangle OAB}\right)_{\min }=2\left(m+n+\sqrt{2mn}\right)
$$

则当 $\dfrac{a}{b}=\dfrac{m+\sqrt{2mn}}{n+\sqrt{2mn}}$ 时取得最小值

此时 $\env{cases}{a=\dfrac{\sqrt{2mn}\left(m+n+\sqrt{2mn}\right)}{n+\sqrt{2mn}}\\b=\dfrac{\sqrt{2mn}\left(m+n+\sqrt{2mn}\right)}{m+\sqrt{2mn}}}$ 

可见 $\mathrm{Mathematica}$ 也不是万能的。

我试了 $\mathrm{FullSimplify}$ 等方法都没能化简，还是靠代入几个根式找规律发现的，因此可能有错误，但画散点图发现差值数量级在 $\pu{E-16}$ 以上，因此我认为是纯粹机器精度的问题。然后最后自己因式分解得出结果。

然而一开始我找规律找出来的结果是 $C_{\min }=2\sqrt{m^2+n^2+4mn+2\left(m+n\right)\sqrt{2mn}}$ ，虽然我眼拙没一下子看出因式分解的方法，但 $\mathrm{Mathematica}$ 居然也没做到。。。

最后~~再找规律~~，得出结果。

---

本来想再{~~化简~>找规律~~}一下 $a,\,b$ 的

最终{~~找到的规律是~>发现~~}
$$
\env{cases}{a=\env{cases}{\dfrac{1}{2m-n}\left[2m^2+(m-n)\sqrt{2mn}\right]&,\,2m\ne n\\ \lim\limits_{\substack{x \to m\\y \to n}}\dfrac{1}{2x-y}\left[2x^2+(x-y)\sqrt{2xy}\right]&,\,2m=n}\\
b=\env{cases}{\dfrac{1}{2n-m}\left[2n^2+(n-m)\sqrt{2mn}\right]&,\,2n\ne m\\ \lim\limits_{\substack{x \to m\\y \to n}}\dfrac{1}{2y-x}\left[2y^2+(y-x)\sqrt{2xy}\right]&,\,2n=m}}
$$

可以简写成

$$
\env{cases}{a=\dfrac{1}{2m-n}\left[2m^2+(m-n)\sqrt{2mn}\right]\\b=\dfrac{1}{2n-m}\left[2n^2+(n-m)\sqrt{2mn}\right]}
$$

可见甚至不如之前的好记，并且还需要多分一类讨论。