# 背包问题

背包问题有些类似很多年以前的购物的综艺节目：如何装满购物车使得物品总价值最大，注意到物品除了价值以外，还有体积属性。

背包（判定）问题询问是否能从一堆物体中找一个子集，使得物品的总体积小于某值，总价值大于某值。

---
**实例：** 有限集合 $U,$ 每个元素 $u \in U,$ 都有相立的长度（体积） $S(u) \in Z^{+}$ 和价值 $V(u) \in Z^{+},$ 并且有常数 $B \in Z^{+}$ 和 $K \in Z^{+}$ 。 

**询问：** 是否存在子集 $U^{\prime} \subseteq U,$ 满足 $\sum_{u \in U} S(u) \leqslant B, \quad \sum_{u \in U} V(u) \geqslant K_{\circ}$

---

该问题可以通过[划分问题](par.html)多项式归约证明为 NPC

## NPC 证明

对背包问题的实例施加限制：对任意 $u \in U,$ 取 $S(u)=V(u)$ 且 $\sum_{u \in U} S(u)$ 为偶数,
取 $B=K=\frac{1}{2} \sum_{u \in U} S(u)$ 。

如此限制的实例为划分问题实例。

> 这里的逻辑有必要重新叙述一遍：对背包问题的实例施加限制后转变为了划分实例，表示的意思是，所有的划分实例都可以看成是背包问题施加了限制后的实例，也即划分实例可以被转换为背包问题实例的一个子集。


## 近似算法性能比



---
1. 将 $n$ 个元素排序得到 $L=\left\{\left(P_{1}, W_{1}\right),\left(P_{2}, W_{2}\right), \cdots,\left(P_{n}, W_{n}\right)\right\},$ 满足:
$$
\frac{P_{1}}{W_{1}} \geqslant \frac{P_{2}}{W_{2}} \geqslant \cdots \geqslant \frac{P_{n}}{W_{n}}
$$
2. 采用贪心算法 $GA,$ 在主次表 $L$ 中，自标号为 1 的元素到标号为 $n$ 的 元素，逐个试装入背包，若标号 $i$ 的元素能装入背包，则取 $x_{i}=1,$ 否 则取 $x_{i}=0$ 。直到不能装入为止，得到一个可行解，其解值为 $G A(I)$ 。
3. 取 $A(I)=\max \left\{G A(I), \max _{1 \leqslant i \leqslant n} P_{i}\right\}$ 所对应的元素装入背包，得实例 $I$ 的可行解。

---

背包问题有多项式时间近似算法 $A,$ 其绝对性能比 $R_{A}<2$ 。 

**证明：**

因为背包问题重量上限为 B，令最优解为 $OPT(I)$，则设正整数 $r$，满足 $\sum_{i=1}^{r} W_{i} \leqslant B, \sum_{i=1}^{r+1} W_{i}>B$。 

易得

$$
O P T(I)<\sum_{i=1}^{r+1} P_{i} \leqslant \sum_{i=1}^{r} P_{i}+\max _{1 \leqslant i \leqslant n} P_{i} \leqslant 2 A(I)
$$

其中因为 $A(I)=\max \left\{G A(I), \max _{1 \leqslant i \leqslant n} P_{i}\right\}$，所以

$$\sum_{i=1}^{r} P_{i}+\max _{1 \leqslant i \leqslant n} P_{i} \leqslant 2 A(I)$$

所以

$$
R_{A}(I)=\frac{O P T(I)}{A(I)}<2
$$

$$R_{A}=\inf \{R_{A}(I) \mid I 为背包问题任意实例 \}<2$$




## 背包问题无多项式时间绝对近似算法的证明

暂略
