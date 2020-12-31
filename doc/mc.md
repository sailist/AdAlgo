# 最小集合覆盖问题（Minimum set Cover）

这又是一个覆盖问题

**实例：** 集合 $S=\left\{s_{1}, \ldots, s_{n}\right\},$ $S$ 的子集的集合 $C=\left\{c_{1}, c_{2}, \ldots, c_{m}\right\},c_i\subset S$

**询问：** 是否存在 $C$ 的子集 $C'$，使 $\left|C^{\prime}\right| \leq k, k \in Z^{+}, \quad U_{c_{i} \in C^{\prime}} c_{i}=S$


## NPC 证明

对 MC 问题添加以下约束，令：

 - $C_i\in C, |C_i|=3$
 - $|S|=3q, K=q$ 
 
经过上述限制后，该问题变成 [X3C](x3c.html) 问题了。

