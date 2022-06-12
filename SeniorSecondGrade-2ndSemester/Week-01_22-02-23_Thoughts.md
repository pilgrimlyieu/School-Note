## 思考

- 2022-02-23

[toc]

### 神秘岛

这可以说是我的童年阴影问题了，小学校本课上看到这个题目，每次想起时都会做噩梦。

#### 原题重现

!!! question [The blue-eyed islanders puzzle](https://terrytao.wordpress.com/2008/02/05/the-blue-eyed-islanders-puzzle/)
    There is an island upon which a tribe resides. The tribe consists of $1000$ people, $100$ of which are blue-eyed and $900$ of which are brown-eyed. 
    Yet, their religion forbids them to know their own eye color, or even to discuss the topic; thus, one resident can see the eye colors of all other residents but has no way of discovering his own (there are no reflective surfaces). 
    If a tribesperson does discover his or her own eye color, then their religion compels them to commit ritual suicide at noon the following day in the village square for all to witness. All the tribespeople are highly logical, highly devout, and they all know that each other is also highly logical and highly devout. 
    One day, a blue-eyed foreigner visits to the island and wins the complete trust of the tribe. 
    One evening, he addresses the entire tribe to thank them for their hospitality. However, not knowing the customs, the foreigner makes the mistake of mentioning eye color in his address, mentioning in his address “how unusual it is to see another blue-eyed person like myself in this region of the world”. 
    What effect, if anything, does this faux pas have on the tribe?

!!! tip Argument 1.
    The foreigner has no effect, because his comments do not tell the tribe anything that they do not already know (everyone in the tribe can already see that there are several blue-eyed people in their tribe).

!!! tip Argument 2.
    100 days after the address, all the blue eyed people commit suicide.

#### 分析

乍一看，外国人没有提供任何信息，岛上有蓝眼睛这件事是众所周知的，所以他的这句话是废话，因此岛上的人不会自杀，即是 **Argument 1** 的结果。

然而真的是这样吗？

有人说这个问题的关键在于区分**共识**与**常识**。在下面我给出定义：

!!! info **共识**
    如果一个群体 $G$ 内所有个体 $p$ 都知道知识 $k$ ，则称知识 $k$ 是群体 $G$ 的**共识**。

!!! info **常识**
    如果一个群体 $G$ 内所有个体 $p$ 都知道知识 $k$ ，且每个个体知道其他个体知道知识 $k$ ，知道其他个体知道其他个体知道知识 $k$ ……，则称知识 $k$ 是群体 $G$ 的**常识**。

但如此看来，外国人还是说了一句废话。「岛上有蓝眼睛」这句话是*共识*，但更是*常识*。

一种常见的推理方法如下

!!! abstract ""
    假设岛上只有 $1$ 个蓝眼睛，有足够多的棕眼睛。那么外国人话音刚落，蓝眼睛看到一片棕眼睛，就会意识到外国人说的是自己，因此蓝眼睛会在第二天（或者说 $1$ 天后）自杀。

    假设岛上有 $2$ 个蓝眼睛，那么 $2$ 个蓝眼睛深情对视，都假设自己不是蓝眼睛，则为对方将要在第二天自杀而感到哀伤。然而第二天两人目瞪口呆，看见对方仍然存活，就知道对方不是唯一的蓝眼睛，即自己也是蓝眼睛，因此 $2$ 人在第三天（或者说 $2$ 天后）自杀。

    依此类推，$n$ 个蓝眼睛将会在第 $n+1$ 天（或者说 $n$ 天后）自杀。

这个推理看起来极为自然，以至于我最初见到这个证明后坚信这是正确的，以至于忽略了 $3$ 个人及以后的推理。在下面我将进行「依此类推」的方法。

我们熟知**数学归纳法**证明命题 $P_i$ 对正整数 $i$ 恒成立的两大要素：
1. 对 $P_1$ 成立
2. 如果对 $P_n$ 成立，那么对 $P_{n+1}$ 也成立

!!! note ""
    假设有 $3$ 个蓝眼睛 $A,\,B,\,C$ ，我们站在上帝视角进行分析：$A$ 运用强大的逻辑推理能力，他假设自己不是蓝眼睛，那么他假设中的 $B$ 将只能看到 $1$ 个蓝眼睛（即 $C$ ），$A$ 假设中的 $B$ 假设自己不是蓝眼睛，那么 $A$ 假设中的 $B$ 假设中的 $C$ 将看不到蓝眼睛。根据「推理一」可知如果 $A$ 假设中的 $B$ 假设成立，那么 $C$ 将在 $1$ 天后自杀。这件事并没有发生，因此 $A$ 假设中的 $B$ 假设不成立，那么 $B$ 就是蓝眼睛了。根据「推理二」知如果 $A$ 假设成立，那么 $B$ （与 $C$ ）将在 $2$ 天后自杀。这件事也没有发生，因此 $A$ 假设不成立，那么 $A$ 就是蓝眼睛了。这个推理同时发生在 $A,\,B,\,C$ 三人身上，因此 $A,\,B,\,C$ 三人将在 $3$ 天后自杀。

    假设有 $n$ 个蓝眼睛 $A_1,\,A_2,\,\ldots ,\,A_n$ ：$A_1$ 假设自己不是蓝眼睛，那么 $A_2$ 就只能看见 $n-1$ 个蓝眼睛，$A_1$ 假设中的 $A_2$ 再假设自己不是蓝眼睛，那么 $A_1$ 假设中的 $A_2$ 假设中的 $A_3$ 就只能看见 $n-2$ 个蓝眼睛，依此类推，$A_1$ 假设中的 $A_2$ 假设中的…… $A_{n-1}$ 假设中的 $A_n$ 将看不到蓝眼睛（这是一个长达 $n$ 的逻辑链条），因此如果 $A_{n-1}$ 假设（省略前置假设，下同）成立，$A_n$ 将在 $1$ 天后自杀，这件事没有发生，因此 $A_{n-1}$ 假设不成立，即 $A_{n-1}$ 是蓝眼睛，根据 $A_{n-2}$ 的假设，$A_{n-1},\,A_n$ 将在 $2$ 天后自杀，这事也没有发生，因此 $A_{n-2}$ 假设不成立，即 $A_{n-2}$ 是蓝眼睛……根据 $A_2$ 的假设，$A_3,\,A_4,\,\ldots ,\,A_n$ 将在 $n-2$ 天后自杀，没有发生，因此 $A_2$ 是蓝眼睛，根据 $A_1$ 的假设，$A_2,\,A_3,\,\ldots ,\,A_n$ 将在 $n-1$ 天后自杀，没有发生，因此 $A_1$ 是蓝眼睛，则 $A_1$ 将在 $n$ 天后自杀。由于这个推理过程发生在所有人身上，因此 $n$ 个蓝眼睛将在 $n$ 天后（或者说第 $n+1$ 天）自杀。

几点需要阐明的地方：

!!! faq 1. 为什么棕眼睛没有自杀？
    容易忽略的是，棕眼睛实际上也进行了上述推理，但由于棕眼睛都能看到 $n$ 个蓝眼睛，而蓝眼睛只能看到 $n-1$ 个蓝眼睛，因此棕眼睛的逻辑链条比蓝眼睛长 $1$ ，而蓝眼睛在完成逻辑链条后的集体自杀终止了棕眼睛的逻辑链条，因此棕眼睛不会自杀。

    当然，我最初看到这个问题时（蓝眼睛和红眼睛）题设还有一个条件，就是岛上只有红蓝眼睛两种，且这是岛民们的*共识*。那么红眼睛就将在 $n+1$ 天后随着蓝眼睛们而去，小岛将变得荒无人烟。

!!! faq 2. 「这件事没有发生」，为什么没有发生？
    因为岛民的逻辑链条还没到底，一旦到底就会自杀，每天这个逻辑链条会前进 $1$ 。

    蓝眼睛由于逻辑链条较短，因此率先自杀。

!!! faq 3. 为什么「岛上有蓝眼睛」这个*常识*能触发逻辑链条？如果没有这个触发，蓝眼睛是否仍会自杀？

    每个人逻辑链条的尾端（开始部分）是 $A_n$ ，在假设中 $A_n$ 将看不到蓝眼睛，因此外国人的话使 $A_n$ 意识到自己是蓝眼睛，因此将会自杀，但没有发生，因此 $A_{n-1}$ 假设错误，$A_{n-1}$ 意识到自己是蓝眼睛……逻辑链条开始前进。

    如果没有这句话，$A_n$ 就不知道自己眼睛颜色，因此逻辑链条就不会触发，因此蓝眼睛就不会自杀。

    此外还要纠正一点，上面讲过的「『岛上有蓝眼睛』这句话是*共识*，但更是*常识*」是<u>错误</u>的！

    「岛上有蓝眼睛」并不是*常识*！

    根据*常识*的定义，$A_1$ 应该要知道 $A_2$ 知道 $A_3$ 知道…… $A_{n-1}$ 知道 $A_n$ 能看见至少 $1$ 个蓝眼睛，才能算是*常识*，但是实际上 $A_1$ 只知道 $A_2$ 知道 $A_3$ 知道…… $A_{n-2}$ 知道 $A_{n-1}$ 能看见至少 $1$ 个蓝眼睛。因此「岛上有蓝眼睛」并不是*常识*！。

#### 无关内容

写本文本部分时，写到*常识*时忘记了缩略语法（想让定义显示为缩略语），去[官方文档](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/)查了一下是`_[缩略语]: 全称`，结果没效果，然后去[插件官网](https://www.npmjs.com/package/markdown-it-abbr)查了才知道是`*[缩略语]: 全称`，效果就像这样：常识。但是没看到将某个地方关闭缩略语的功能。

然后再扫了一眼官方文档，看到一个奇奇怪怪的语法叫 Admonition，而且还没给用法，好在下面给了一个[网站](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)介绍了这个的用途。结果我一看，* 炸天啊！这真的太漂亮了！！！

语法是
```
!!! 类型 标题（为 "" 时不显示标题）
    内容

    内容
```

以下举出所有支持的类型与类型名称：

!!! note Note(default)
    `note`

!!! abstract
    `abstract`, `summary`, `tldr`

!!! info
    `info`, `todo`

!!! tip
    `tip`, `hint`, `important`

!!! success
    `success`, `check`, `done`

!!! question
    `question`, `help`, `faq`

!!! warning
    `warning`, `caution`, `attention`

!!! failure
    `failure`, `fail`, `missing`

!!! danger
    `danger`, `error`

!!! bug
    `bug`

!!! example
    `example`

!!! quote
    `quote`, `cite`

!!! note "" 
    No Tile (Type is *Note*)

这不比引用语法 `>` 漂亮一亿倍？引用语法出来挨打：
> 我是丑陋的引用

看了文档介绍，发现还支持 Inline blocks, `???`, `???+` 等功能，可惜 MPE 没有加入。Inline blocks 应该就是可以将 Admonition 放在左侧或右侧，`???` 就是可以折叠 Admonition，默认折叠，`???+` 默认展开。

然后这个文档还介绍了其他插件，MPE 不支持而我又挺喜欢的有：

!!! example Annotations
    ```md
    Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
    { .annotate }

    1.  :man_raising_hand: I'm an annotation! I can contain `code`, __formatted
        text__, images, ... basically anything that can be expressed in Markdown.
    ```
    ![](images/2022-02-23-11-54-17.png)

!!! example Content tabs
    ```md
    === "C" 
        ```c
        #include <stdio.h>

        int main(void) {
        printf("Hello world!\n");
        return 0;
        }
        ```
    === "C++"
        ```c++
        #include <iostream>

        int main(void) {
        std::cout << "Hello world!" << std::endl;
        return 0;
        }
        ```
    ```
    ![](images/2022-02-23-11-54-51.png)

!!! example Images
    这个其实支持，只不过插件还支持图片位置设置等。
    ![](images/2022-02-23-11-58-35.png)
    ![](images/2022-02-23-11-58-05.png)
    ![](images/2022-02-23-11-58-58.png)
    然而图片标题仍然无法实现
    ![](images/2022-02-23-11-59-45.png)

还有一个 MPE 支持的功能（但没在文档见到）：**定义功能**

语法为：

```md
名词
:   释义
```

渲染为：

名词
:   释义

英文加 ` 或许好看一点：

`Lorem ipsum dolor sit amet`
:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

Lorem ipsum dolor sit amet
:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

本来想用这个来定义共识和常识，但是无奈 Admonitions 太好看了，就用 info 来代替了。

### 鸡蛋硬度

#### 原题

!!! question 鸡蛋硬度
    假如你有两个硬度相同的鸡蛋🥚，你想要测试它们的硬度。有一栋一百层高的楼，你可以选择某一层将鸡蛋掷下，最高的能使鸡蛋不破裂的层数就称为鸡蛋的硬度。假设鸡蛋的硬度在 $0-100$ （若第一层就破裂硬度为 $0$ ，若第一百层鸡蛋仍不破裂硬度为 $100$ ）。请找到一个最优策略，并计算其最坏情况所需掷的次数。

#### [思路](http://www.math345.com/blog/article/14)

不妨反向思考，假如最多允许掷 $n$ 次，那么最高能测试多少层？

第一次从 $n$ 层掷，如果碎了，就从第 $1$ 层开始一层一层往上掷，最坏情况就是 $n-1$ 时碎了，用时最多 $n$ 次。

如果没碎，就到 $n+(n-1)$ 层掷，如果碎了就从第 $n+1$ 开始掷，最坏情况就是 $n+(n-1)-1$ 时碎了，用时最多 $n$ 次。

持续 $n$ 次，最多能测试 $N={\displaystyle \sum_{i=1}^{n}i=\dfrac{n(n+1)}{2}}$ 层。

回到原题，即 $N\ge 100$ 得 $n\ge 14$ ，因此最坏情况所需掷的次数为 $14$ 

#### 拓展

假设有 $m$ 个鸡蛋，定义 $N_m(n)$ 为 $n$ 次测试能测试的最多楼层。

第一次应该从 $\left(N_{m-1}(n-1)+1\right)$ 层掷，如果碎了，就从第一层开始掷。

如果没碎，第二次应该从 $\left(N_{m-1}(n-1)+1\right)+\left(N_{m-1}(n-2)+1\right)$ 层掷，如果碎了，就从 $\left(N_{m-1}(n-1)+1\right)+1$ 层开始掷。

持续 $n$ 次，则 $N_m(n)={\displaystyle \sum_{i=0}^{n-1}N_{m-1}(i)+n}$ 

则
$$
\env{aligned}{N_0(n)&=0\\
N_1(n)&=n\\
N_2(n)&=\dfrac{1}{2}n^2+\dfrac{1}{2}n\\
N_3(n)&=\dfrac{1}{6}n^3+\dfrac{5}{6}n\\
N_4(n)&=\dfrac{1}{24}n^4-\dfrac{1}{12}n^3+\dfrac{11}{24}n^2+\dfrac{7}{12}n}
$$

显然当 $m>0$ 时 $N_m^{(m)}(n)=\dfrac{1}{m!}$ 

其他规律找不到了。

*[共识]: 如果一个群体 G 内所有个体 p 都知道知识 k ，则称知识 k 是群体 G 的共识。

*[常识]: 如果一个群体 G 内所有个体 p 都知道知识 k ，且每个个体知道其他个体知道知识 k ，知道其他个体知道其他个体知道知识 k ……，则称知识 k 是群体 G 的常识。