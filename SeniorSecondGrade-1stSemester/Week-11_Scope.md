## 偏移法[^自定义名称]解决圆锥曲线斜率之积/斜率之和为定值过定点问题

[toc]

- [x] $\Anki$ 

### 斜率之积为定值

#### 椭圆

椭圆 $C:\:\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1$ 上有一点 $A\left(x_0, y_0\right)$ ，过 $A$ 作两条直线 $AM,\,AN$ 交 $C$ 于 $M,\,N$ ，且满足 $k_{AM}\cdot k_{AN}=r\quad\left(r\ne \dfrac{b^2}{a^2}\right)$ ，则 $MN$ 过定点 $P\left(\dfrac{ra^2+b^2}{ra^2-b^2}x_0, \dfrac{-(ra^2+b^2)}{ra^2-b^2}y_0\right)$ 

![](images/Scope-Figure-1.png)

以 $A$ 为坐标原点仿建坐标系 $\alpha$ ，则 $C_{\alpha}:\:\dfrac{(x+x_0)^2}{a^2}+\dfrac{(y+y_0)^2}{b^2}=1$ ，展开得 $b^2x^2+a^2y^2+2x_0b^2x+2y_0a^2y=0$ 

设 $l_{\alpha}:\:mx+ny=1$ ，易见 $l_{\alpha}$ 不过 $A_{\alpha}\left(0,0\right)$ 。将 $l_{\alpha}$ 代入原式

$$
\env{aligned}{&\Rightarrow b^2x^2+a^2y^2+2\left(x_0b^2x+y_0a^2y\right)\left(mx+ny\right)=0\\&\Rightarrow \left(b^2+2mx_0b^2\right)x^2+\left(a^2+2ny_0a^2\right)y^2+2\left(nx_0b^2+my_0a^2\right)xy=0\\&\Rightarrow \left(a^2+2ny_0a^2\right)\dfrac{y^2}{x^2}+2\left(nx_0b^2+my_0a^2\right)\dfrac{y}{x}+\left(b^2+2mx_0b^2\right)=0\\&\Rightarrow \prod \dfrac{y}{x}=k_{AM}\cdot k_{AN}=\dfrac{b^2\left(2mx_0+1\right)}{a^2(2ny_0+1)}=r\\&\Rightarrow n=\dfrac{b^2(2mx_0+1)-ra^2}{2ry_0a^2}}
$$

将 $n$ 代入 $l_{\alpha}:\:mx+ny=1$ 得

$$
\env{aligned}{&\Rightarrow 2rmy_0a^2x+\left(b^2-ra^2+2mx_0b^2\right)y=2ry_0a^2\\&\Rightarrow \text{过定点}\env{cases}{x=\dfrac{-2b^2x_0}{b^2-ra^2}\\y=\dfrac{2ra^2y_0}{b^2-ra^2}}}
$$

即 $P_{\alpha}\left(\dfrac{-2b^2x_0}{b^2-ra^2}, \dfrac{2ra^2y_0}{b^2-ra^2}\right)$ 

即 $P\left(\dfrac{ra^2+b^2}{ra^2-b^2}x_0, \dfrac{-\left(ra^2+b^2\right)}{ra^2-b^2}y_0\right)$ 

#### 双曲线

双曲线 $C:\:\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}=1$ 上有一点 $A\left(x_0, y_0\right)$ ，过 $A$ 作两条直线 $AM,\,AN$ 交 $C$ 于 $M,\,N$ ，且满足 $k_{AM}\cdot k_{AN}=r\quad\left(r\ne -\dfrac{b^2}{a^2}\right)$ ，则 $MN$ 过定点 $P\left(\dfrac{ra^2-b^2}{ra^2+b^2}x_0, \dfrac{-(ra^2-b^2)}{ra^2+b^2}y_0\right)$ 

![](images/Scope-Figure-2.png)

同理，过程略。

#### 抛物线

设抛物线 $C:\:y^2=2px$ 上一点 $A\left(x_0, y_0\right)$ ，过 $A$ 作两条直线 $AM,\,AN$ 交 $C$ 于 $M,\,N$ ，且满足 $k_{AM}\cdot k_{AN}=r\quad\left(r\ne 0\right)$ ，则 $MN$ 过定点 $P\left(x_0-\dfrac{2p}{r}, -y_0\right)$ 

![](images/Scope-Figure-3.png)

以 $A$ 为坐标原点仿建坐标系 $\alpha$ ，则 $C_{\alpha}:\:(y+y_0)^2=2p\left(x+x_0\right)$ ，展开得 $y^2+2(y_0y-px)=0$ 

设 $l_{\alpha}:\:mx+ny=1$ ，易见 $l_{\alpha}$ 不过 $A_{\alpha}\left(0,0\right)$ 。将 $l_{\alpha}$ 代入原式

$$
\env{aligned}{&\Rightarrow y^2+2\left(y_0y-px\right)\left(mx+ny\right)=0\\&\Rightarrow \left(2ny_0+1\right)y^2-2mpx^2+2(my_0-np)xy=0\\&\Rightarrow \left(2ny_0+1\right)\dfrac{y^2}{x^2}+2\left(my_0-np\right)\dfrac{y}{x}-2mp=0\\&\Rightarrow \prod \dfrac{y}{x}=k_{AM}\cdot k_{AN}=\dfrac{-2mp}{2ny_0+1}=r\\&\Rightarrow m=\dfrac{-r\left(2ny_0+1\right)}{2p}}
$$

将 $m$ 代入 $l_{\alpha}:\:mx+ny=1$ 得

$$
\env{aligned}{&\Rightarrow \left(2rny_0+r\right)x-2npy=-2p\\&\Rightarrow \text{过定点}\env{cases}{x=-\dfrac{2p}{r}\\y=-2y_0}}
$$

即 $P_{\alpha}\left(-\dfrac{2p}{r}, -2y_0\right)$ 

即 $P\left(x_0-\dfrac{2p}{r}, -y_0\right)$ 

### 斜率之和为定值

#### 椭圆

椭圆 $C:\:\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1$ 上一点 $A\left(x_0, y_0\right)$ ，过 $A$ 作两条直线 $AM,\,AN$ 交 $C$ 于 $M,\,N$ ，且满足 $k_{AM}+k_{AN}=s\quad\left(s\ne 0\right)$ ，则 $MN$ 过定点 $P\left(x_0-\dfrac{2}{s}y_0, -\dfrac{2b^2}{sa^2}x_0-y_0\right)$ 

![](images/Scope-Figure-4.png)

以 $A$ 为坐标原点仿建坐标系 $\alpha$ ，则 $C_{\alpha}:\:\dfrac{(x+x_0)^2}{a^2}+\dfrac{(y+y_0)^2}{b^2}=1$ ，展开得 $b^2x^2+a^2y^2+2x_0b^2x+2y_0a^2y=0$ 

设 $l_{\alpha}:\:mx+ny=1$ ，易见 $l_{\alpha}$ 不过 $A_{\alpha}\left(0,0\right)$ 。将 $l_{\alpha}$ 代入原式

$$
\env{aligned}{&\Rightarrow b^2x^2+a^2y^2+2\left(x_0b^2x+y_0a^2y\right)\left(mx+ny\right)=0\\&\Rightarrow \left(b^2+2mx_0b^2\right)x^2+\left(a^2+2ny_0a^2\right)y^2+2\left(nx_0b^2+my_0a^2\right)xy=0\\&\Rightarrow \left(a^2+2ny_0a^2\right)\dfrac{y^2}{x^2}+2\left(nx_0b^2+my_0a^2\right)\dfrac{y}{x}+\left(b^2+2mx_0b^2\right)=0\\&\Rightarrow \sum \dfrac{y}{x}=k_{AM}+k_{AN}=\dfrac{-2\left(nx_0b^2+my_0a^2\right)}{a^2(2ny_0+1)}=s\\&\Rightarrow m=\dfrac{-\left(2sny_0a^2+sa^2+2nx_0b^2\right)}{2y_0a^2}}
$$

将 $m$ 代入 $l_{\alpha}:\:mx+ny=1$ 得

$$
\env{aligned}{&\Rightarrow \left(2sny_0a^2+sa^2+2nx_0b^2\right)x-2ny_0a^2y=-2y_0a^2\\&\Rightarrow \text{过定点}\env{cases}{x=-\dfrac{2y_0}{s}\\y=-\dfrac{2b^2x_0}{sa^2}-2y_0}}
$$

即 $P_{\alpha}\left(-\dfrac{2}{s}y_0, -\dfrac{2b^2}{sa^2}x_0-2y_0\right)$ 

即 $P\left(x_0-\dfrac{2}{s}y_0, -\dfrac{2b^2}{sa^2}x_0-y_0\right)$ 

#### 双曲线

设双曲线 $C:\:\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}=1$ 上一点 $A\left(x_0, y_0\right)$ ，过 $A$ 作两条直线 $AM,\,AN$ 交 $C$ 于 $M,\,N$ ，且满足 $k_{AM}+k_{AN}=s\quad\left(s\ne 0\right)$ ，则 $MN$ 过定点 $P\left(x_0-\dfrac{2}{s}y_0, \dfrac{2b^2}{sa^2}x_0-y_0\right)$ 

![](images/Scope-Figure-5.png)

同理，过程略。

#### 抛物线

设抛物线 $C:\:y^2=2px$ 上一点 $A\left(x_0, y_0\right)$ ，过 $A$ 作两条直线 $AM,\,AN$ 交 $C$ 于 $M,\,N$ ，且满足 $k_{AM}+k_{AN}=s\quad(s\ne 0)$ ，则 $MN$ 过定点 $P\left(x_0-\dfrac{2}{s}y_0, \dfrac{2p}{s}-y_0\right)$ 

![](images/Scope-Figure-6.png)

以 $A$ 为坐标原点仿建坐标系 $\alpha$ ，则 $C_{\alpha}:\:(y+y_0)^2=2p\left(x+x_0\right)$ ，展开得 $y^2+2(y_0y-px)=0$ 

设 $l_{\alpha}:\:mx+ny=1$ ，易见 $l_{\alpha}$ 不过 $A_{\alpha}\left(0,0\right)$ 。将 $l_{\alpha}$ 代入原式

$$
\env{aligned}{&\Rightarrow y^2+2\left(y_0y-px\right)\left(mx+ny\right)=0\\&\Rightarrow \left(2ny_0+1\right)y^2-2mpx^2+2(my_0-np)xy=0\\&\Rightarrow \left(2ny_0+1\right)\dfrac{y^2}{x^2}+2\left(my_0-np\right)\dfrac{y}{x}-2mp=0\\&\Rightarrow \sum \dfrac{y}{x}=k_{AM}+k_{AN}=\dfrac{2\left(np-my_0\right)}{2ny_0+1}=s\\&\Rightarrow m=\dfrac{2np-2sny_0-s}{2y_0}}
$$

将 $m$ 代入 $l_{\alpha}:\:mx+ny=1$ 得

$$
\env{aligned}{&\Rightarrow \left(2np-2sny_0-s\right)x+2ny_0y=2y_0\\&\Rightarrow \text{过定点}\env{cases}{x=-\dfrac{2y_0}{s}\\y=\dfrac{2p}{s}-2y_0}}
$$

即 $P_{\alpha}\left(-\dfrac{2}{s}y_0, \dfrac{2p}{s}-2y_0\right)$ 

即 $P\left(x_0-\dfrac{2}{s}y_0, \dfrac{2p}{s}-y_0\right)$ 

[^自定义名称]: 即**齐次化联立**