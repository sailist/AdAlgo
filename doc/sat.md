# 布尔可满足性问题（Boolean satisfiability problem, SAT）

SAT 问题属于决定性问题，也是第一个被证明属于NP完全的问题，1970年 Cook 证明 SAT 问题是NP-完全问题。即Cook定理。Cook说明若SAT多项式时间可解，则所有NP问题多项式时间可解。

Cook定理证明 SAT 问题属于 NPC 问题的核心步骤：
1. 证明 SAT 问题属于 NP 问题，这明显成立（给定一个真值指派，按顺序求解即可）
2. 证明其他所有属于 NP 类的判定问题都可以通过某多项式变换变换为 SAT 问题




## SAT 问题


**实例**

布尔变量集合 
$$U=\left\{u_{1}, u_{2}, \cdots, u_{n}\right\},$$ 
项集合（也就是多个布尔变量或其取反后的布尔变量构成的集合）
$$C=\left\{C_{1}, C_{2}, \cdots, C_{m}\right\},$$
其中
$$C_{i}=\left\{u[i, 1], \cdots, u\left[i, k_{i}\right]\right\}
\subseteq U \cup \vec{U}, \quad \bar{U}=\left\{\bar{u}_{1}, \cdots, \bar{u}_{n}\right\}$$

**询问** 是否存在 $U$ 的真值指派: 
$U \rightarrow\{\mathrm{F}, \mathrm{T}\},$ 满足 

$$\bigwedge_{i=1}^{m}\left(\sum_{j=1}^{k_{i}} u[i, j]\right)=\mathrm{T}$$


## 证明方法简述

构造多项式时间复杂度（为 P(n)）的 NTM 可计算程序 M，我们发现可以用有限个布尔变量表示每个时刻 M 的状态，同时可以用有限个项描述 M 的执行过程。

而证明 SAT 是 NPC 的核心思路，是证明


说明方法（详细推导略）：

1. 所有项包含的布尔变量数量均不超过所给布尔变量数目的 2 倍
2. 项集合的数量为 O(P3(n))
3. 布尔变量集合的布尔变量数量为 O(P(n)) 

最终可以得到变换的时间复杂性为 O(P4(n))，仍然是多项式时间。
