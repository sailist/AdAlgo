# 多任务排工（multi-task scheduling）问题


---
**实例：** 有限任务的集合 $A,$ 每个任务 $a \in A,$ 都有相应的加工时间长度 $L(a) \in Z^{+}$。 加工任务机器数为 $m \in Z^{+},$ 加工的最后期限 $D \in Z^{+}$ 。 

**询问：** 是否存在 $A$ 的划分 $A=A_{1} \cup A_{2} \cup \cdots \cup A_{m}, A_{i} \cap A_{j}=\varnothing, \quad 1 \leqslant i, j \leqslant m, \quad i \neq j,$ 使得
$$
\max \left\{\sum_{a \in A_{i}} L(a) \mid 1 \leqslant i \leqslant m\right\} \leqslant D
$$

---
该任务可以通过[划分问题](par.html)多项式归约证明。

## NPC 证明

对多任务排工问题的实例施加限制为，置 $m=2, \quad \sum_{a \in A} L(a)$ 为偶数， 且满足

$$D=\frac{1}{2} \sum_{a \in A} L(a)$$

这样限制后的实例成为划分问题的实例。