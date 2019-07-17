## 基本计数原理

**加法原理** 假设事件E能以m种方式出现，事件F能以n种方式出现，且两种事件不能同时出现，那么 E或F 能以m+n种方式出现。

推广到一般情况，假设事件E1 能以n1种方式出现，事件E2 能以n2种方式出现，……，且任意两个事件不能同时出现，
那么事件 E1,E2,... 之一 以 n1 + n2 + ... 种方式出现。

**乘法原理** 假设事件E能以m种方式发生，独立于事件E之外的事件F能以n种方式发生，那么 E和F的组合有以mn种方式发生。

推广到一般情况，互相独立的事件E1，E2 ... 分别有 n1，n2，...种方式发生，那么所有事件依照指定顺序 有 n1 n2 n3 ...种方式发生。

### 集合论的解释

  1. **加法原理** 若 A 与 B 不相交，则
    $$
    \textrm{card}(A \cup B) = \textrm{card}(A) + \textrm{card}(B)
    $$




## 阶乘符号

从 1 到 n（包括 1 和 n）的正整数的积记作 n! (读作n的阶乘)；即：
$$
n! = 1 * 2 * 3 * (n - 2)(n - 1) n
$$

也可以定义为：

    1. 1!= 1
    2. n! = n * (n - 1)!
    3. 0! = 1

## 二项式符号

设 r 和 n 为正整数，r <= n，符号(n,r)（读作 nCr） 定义为：

$$
\binom{n}{r} = \frac{n (n - 1) (n - 2)\cdots (n - r + 1)}{1 \cdot 2 \cdot \cdots (r - 1) \cdot r}
$$

即：

$$
\binom{n}{r}= \frac{n!}{r! (n - r)!}
$$

由于 n - (n - r) = r，因此有：

$$
\binom{n}{n - r} = \binom{n}{r}
$$

亦即，
$$
a + b = n \implies \binom{n}{a} = \binom{n}{b}
$$

### 二项式系数与Pascal三角形

$\binom{n}{r}$ 称为**二项式系数**，因为它们作为 (a + b)^n 的展开式的系数出现。特别地，可以证明：

$$
(a + b) ^n = \sum_{k = 0}^{n} \binom{n}{k} a^{n - k}b^k
$$

a + b 的相继幂的系数可以排成三角形的数表，称为Pascal三角形。Pascal形角形中的数有如下交互性质：

    1. 每一行的每一个数与最后一个数都是 1
    2. 数表中的每个其他数可通过相加位于其上方的两数得到。

**定理6.1**

$$
\binom{n+1}{r} = \binom{n}{r - 1} + \binom{n}{r}
$$

## 排列

n个对象以给定次序的任一安排称为这些对象（同时取出全部）的排列。n个对象中的任r个对象以给定序的任一安排称为 r-排列，或称为 n个对象的排列。

n个对象取r个的排列数记为：
$$
p(n, r), nPr, P_{nr}, P_r^n, (n)_r
$$

**P(n, r)公式的推导**

**定理6.2**

$$
P(n, r) = \frac{n!}{(n - r)!}
$$

**推论6.3**

n个对象（同时全取）的排列数为n!

### 可重排列

通常我们想知道可重集的排列数，可重集是指有某些元素相同的集合，用

$$
P(n; n_1, n_2,\cdots, n_r)=\binom{n}{n_1\quad n_2\quad\cdots\quad n_r}
$$

表示n个对象的排列数。其中n_1个对象是相同的，n_2个对象是相同的，...，n_r个对象是相同的。

**定理6.4**

$$
P(n; n_1, n_2, \cdots, n_r) = \frac{n!}{n_1! n_2! \cdots n_r!}
$$

## 组合

设有含n个对象的集合，n个对象取r个对象的组合是r个对象的不计次序的任一选取。
换句话说，n个对象的任一个 r-元素子集是一个r-组合。

n个对象取r个的组合数记为C(n, r)。也可以记为：

$$
nC_r, C_{nr}, C_r^n
$$

**C(n, r)公式**

由于 n 个对象取r个的任一组合确定了该组合中的对象 r! 个排列，因此有：

$$
P(n, r) = r!C(n, r)
$$

**定理6.5**

$$
C(n, r) = \frac{P(n, r)}{r!} = \frac{n!}{r! (n - r)!}
$$

因此：
$$
C(n, r) = \binom{n}{r}
$$

### 可重组合

$n$ 个元素的集合中允许重复的 $r$ 组合有
$$
\binom{n+r-1}{r}
$$
种

## 鸽笼原理

若 n 个鸽笼被 n + 1 只或更多只鸽子占据，则至少有一个鸽笼被超过一只鸽子占据。

**推广的鸽笼原理**

若$n$个鸽笼被 $kn + 1$ 只或更多只鸽子占据，k为正整数，则至少有一个鸽笼被 $k+1$ 只或更多只鸽子占据。

## 容斥原理

设A，B为两个有限集，则

$$
\text{card}(A\cup B) = \text{card}(A) + \text{card}(B) - \text{card}(A \cap B)
$$

**定理 6.6** 对任意有限集A，B，C，有
$$
n(A\cup B \cup C) = n(A) + n(B) + n(C)
 - n(A\cap B) - n(A\cap C) - n(B\cap C)
 + n(A\cap B \cap C)
$$

**定理6.7**

假设A1, A2, ..., Am为有限集，今Sk表示给定m个集合的所有可能的 k 个交的基数

$$
\text{n}(A_{i_1} \cap A_{i_2} \cap \cdots \cap A_{i_k})
$$

的和，则

$$
n(A_1 \cup A_2 \cup \cdots \cup A_m) = s_1 - s_2 + s_3 + (-1)^{m - 1} s_m
$$

## 有序划分与无序划分

**有序划分**

**定理6.8** 设A有n个元素，n_1, n_2, ..., n_r 是正整数，它们的和为n，即 n_1 + n_2 + ... + n_r = n，
则 A 的形如[A_1, A_2, ..., A_r]的有限划分有：

$$
\frac{n!}{n_1! n_2! \cdots n_r!}
$$

个，其中 A_1 含有 n_1 个元素，A_2 含有 n_2 个元素，...,A_r 含有 n_r 个元素。

**无序划分**

在有限划分的基础上，除以组数的全排列数（即 r! ）。

# 高级计数技术

从某些前项求后项的规则叫做 **递推关系**

## 线性递推关系

一个常系数的 $k$ 阶线性齐次递推关系形如
$$
a_{n}=c_{1} a_{n-1}+c_{2} a_{n-2}+\cdots+c_{k} a_{n-k}
$$

### 特征方程

方程
$$
r^{k}-c_{1} r^{k-1}-c_{2} r^{k-2}-\cdots-c_{k-1} r-c_{k}=0
$$
称为该递推关系的 **特征方程**, 它的解称为该递推关系的 **特征根**.

假设该方程有 $k$ 个不相等的实根 $r_{1}, r_{2}, \cdots, r_{k}$, 那么
$$
a_{n}=\alpha_{1} r_{1}^{n}+\alpha_{2} r_{2}^{n}+\cdots+\alpha_{k} r_{k}^{n}
$$
其中诸 $\alpha$ 的值由该递推关系的初始值解得.

更一般地, 假设该方程有 $t$ 个不相等的根 $r_{1}, r_{2}, \cdots, r_{t}$, 其重数分别为 $m_{1}, \quad m_{2}, \cdots, \quad m_{t}$, 那么
$$
\begin{aligned} a_{n}=&\left(\alpha_{1,0}+\alpha_{1,1} n+\cdots+\alpha_{1, m_{1}-1} n^{m_{1}-1}\right) r_{1}^{n} \\ &+\left(\alpha_{2,0}+\alpha_{2,1} n+\cdots+\alpha_{2, m_{1}-1} n^{m_{1}-1}\right) r_{2}^{n} \\ &+\cdots+\left(\alpha_{t, 0}+\alpha_{t, 1} n+\cdots+\alpha_{t, m_{i}-1} n^{m_{i}-1}\right) r_{t}^{n} \end{aligned}
$$
对于常系数线性但非齐次的递推关系, 如
$$
a_{n}=c_{1} a_{n-1}+c_{2} a_{n-2}+\cdots+c_{k} a_{n-k}+F(n)
$$
递推关系 $a_{n}=\alpha_{1} r_{1}^{n}+\alpha_{2} r_{2}^{n}+\cdots+\alpha_{k} r_{k}^{n}$ 称为 **相伴的齐次线性递推关系**.

如果 $\left\{a_{n}^{(p)}\right\}$ 是非齐次递推关系的一个特解, 那么它的每一个解都是 $\left\{a_{n}^{(p)}+a_{n}^{(h)}\right\}$ 的形式, 其中 $a_{n}^{(h)}$ 是相伴的齐次线性递推关系的一个解.

当 $F(n)$ 的形式形如
$$
F(n)=\left(b_{t} n^{t}+b_{t-1} n^{t-1}+\cdots+b_{1} n+b_{0}\right) s^{n}
$$
我们可以知道它的一个特解
$$
\left(p_{t} n^{t}+p_{t-1} n^{t-1}+\cdots+p_{1} n+p_{0}\right) s^{n}
$$
当 $s$ 是相伴的递推关系特征方程的解时, 设它的重数为 $m$, 特解为
$$
n^{m}\left(p_{t} n^{t}+p_{t-1} n^{t-1}+\cdots+p_{1} n+p_{0}\right) s^{n}
$$

## 分治算法

假设一个递归算法把一个规模为 $n$ 的问题分为 $a$ 个规模为 $n/b$ 的小问题, 此外, 该算法还需要 $g(n)$ 的额外运算来合并小问题的解, 即为
$$
f(n)=a f(n / b)+g(n)
$$

### 主定理

设 $f$ 满足递推关系
$$
f(n)=a f(n / b)+c n^{d}
$$
那么
$$
f(n)=\left\{\begin{array}{ll}{O\left(n^{d}\right)} & {a<b^{d}} \\ {O\left(n^{d} \log n\right)} & {a=b^{d}} \\ {O\left(n^{\log _{b} a}\right)} & {a>b^{d}}\end{array}\right.
$$

生成函数

实数序列 $a_{0}, \quad a_{1}, \cdots, a_{k}, \dots$ 的生成函数是无穷级数
$$
G(x)=a_{0}+a_{1} x+\cdots+a_{k} x^{k}+\cdots=\sum_{k=0}^{\infty} a_{k} x^{k}
$$

### 广义二项式系数

设 $u$ 是实数且 $k$ 是非负整数. 那么广义二项式系数 $\left(\begin{array}{l}{u} \\ {k}\end{array}\right)$ 定义为
$$
\binom u k=\left\{\begin{array}{ll}{u(u-1) \cdots(u-k+1) / k !} & {k>0} \\ {1} & {k=0}\end{array}\right.
$$

### 广义二项式定理

设 $x$ 是实数, $|x|<1$, $u$ 是实数
$$
(1+x)^{u}=\sum_{k=0}^{\infty}\left(\begin{array}{l}{u} \\ {k}\end{array}\right) x^{k}
$$

### 计数问题与生成函数



## 容斥原理

设 $A_{1}, A_{2}, \cdots, A_{n}$ 是有穷集, 那么
$$
\left|A_{1} \cup A_{2} \cup \cdots \cup A_{n}\right|=\\
\sum_{1 \leq i \leq n}\left|A_{i}\right|-\sum_{1 \leqslant i<j \leqslant n}\left|A_{i} \cap A_{j}\right|+\sum_{1<i<j<k<n}\left|A_{i} \cap A_{j} \cap A_{k}\right|-\cdots+(-1)^{n+1}\left|A_{1} \cap A_{2} \cap \cdots \cap A_{n}\right|
$$
