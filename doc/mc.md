# 最小集合覆盖问题（Minimum set Cover）

这又是一个覆盖问题，不同的是，该问题只要求覆盖，不要求严格覆盖。

**实例：** 集合 $S=\left\{s_{1}, \ldots, s_{n}\right\},$ $S$ 的子集的集合 $C=\left\{c_{1}, c_{2}, \ldots, c_{m}\right\},c_i\subset S$

**询问：** 是否存在 $C$ 的子集 $C'$，使 $\left|C^{\prime}\right| \leq k, k \in Z^{+}$，且

$$
[ \bigcup_{c_{i} \in C^{\prime}} c_i]=S
$$


## NPC 证明

对 MC 问题添加以下约束，令：

 - 对任意 $c_i\in C, |c_i|=3$
 - 令 $|S|=3q$ 
 - $K=q$ （该约束使得覆盖必须为严格覆盖）
 
经过上述限制后，该问题变成 [X3C](x3c.html) 问题了。

