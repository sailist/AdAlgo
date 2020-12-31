# 3SAT 问题

3SAT 问题基于 [SAT](sat.html) 问题添加了一个额外约束，即要求每一个项集合由三个元素组成 $|C_i|=3$。

**实例**

布尔变量集合 
$$U=\left\{u_{1}, u_{2}, \cdots, u_{n}\right\},$$ 
项集合（也就是多个布尔变量或其取反后的布尔变量构成的集合）
$$C=\left\{C_{1}, C_{2}, \cdots, C_{m}\right\},$$
其中
$$C_{i}=\left\{u[i, 1], \cdots, u\left[i, k_{i}\right]\right\}
\subseteq U \cup \vec{U}, \quad \bar{U}=\left\{\bar{u}_{1}, \cdots, \bar{u}_{n}\right\},\color{red}{|C_i|=3}$$

**询问** 是否存在 $U$ 的真值指派: 
$U \rightarrow\{\mathrm{F}, \mathrm{T}\},$ 满足 

$$\bigwedge_{i=1}^{m}\left(\sum_{j=1}^{k_{i}} u[i, j]\right)=\mathrm{T}$$

该问题首先是 NP 问题，接下来，通过将 SAT 问题归约到 3SAT 问题来证明 3SAT 是 NPC。

归约的核心思路是对 [SAT](sat.html) 问题实例中的项集合中的项元素进行变换，使得大小不是 3 的项元素通过某种方式转变为 1个或多个大小为 3 的项元素

## NPC 证明

将不是由 3 个布尔变量组成的项被转换为等价的、由 3 个布尔变量组成的等价项，需要分情况讨论。

## K=1
$$ C_1=\{z_1\} $$
对这种情况，可以在布尔变量集合中增加两个布尔变量 ${y11, y12}$，把 $C_1$ 变换为 4 个包含三个布尔变量的项（注意四恰好是两个布尔变量的可能性组合数，即构造方法）：

$$
\begin{array}{c}

\left\{z_{1}, y_{j}^{(1)}, y_{j}^{(2)}\right\}, \quad\left\{z_{1}, y_{j}^{(1)}, \bar{y}_{j}^{(2)}\right\}, \quad\left\{z_{1}, \bar{y}_{j}^{(1)}, y_{j}^{(2)}\right\}, \quad\left\{z_{1}, \bar{y}_{j}^{(1)}, \bar{y}_{j}^{(2)}\right\}
\end{array}
$$

## k=2
$$C_1=\{z_1,z_2\}$$

新增 1 个布尔变量，拆成两项：

$$
\left\{z_{1}, z_{2}, y_{j}^{(1)}\right\},\left\{z_{1}, z_{2}, \bar{y}_{j}^{(1)}\right\}
$$

## k=3
保持原样

## k=4
$$C_1=\{z_1,z_2,z_3,z_4\}$$

增加一个布尔变量，拆成两项（2-2 分到两个项中）：

$$
\left\{z_{1}, z_{2}, y_{j}^{(1)}\right\},\left\{z_{3}, z_{4}, \bar{y}_{j}^{(1)}\right\}
$$

## k=5

$$C_1=\{z_1,z_2,...,z_5\}$$

增加两个布尔变量，拆成3项（上述的5个元素分别分 2,2,1 个到这三项中）：

$$
\left\{z_{1}, z_{2}, y_{j}^{(1)}\right\},\left\{z_{4}, z_{5}, \bar{y}_{j}^{(2)}\right\},\left\{z_{3},y_{j}^{(2)} , \bar{y}_{j}^{(1)}\right\}
$$


## k>3 
发现 $k>3$ 以上的情况可以进行归纳，即新增 $k-3$ 个布尔变量，从头尾各自拆出两个元素和一个新增布尔变量的一种情况分在一起，然后中间的元素每一个和两个新增布尔变量的一种情况分在一起，即

$$
\begin{array}{c}
C^{\prime}[j]=\left\{\left\{z_{1}, z_{2}, y_{j}^{(1)}\right\},\left\{\bar{y}_{j}^{(k-3)}, z_{k-1}, z_{k}\right\}\right\} \\
\cup\left\{\left\{\bar{y}_{j}^{(i)}, z_{i+2}, y_{j}^{(i+1)}\right\} \mid 1 \leqslant i \leqslant k-4\right\}
\end{array}
$$



通过更具体的证明可得，对于上述的所有情况：
1. 存在真值指派使 SAT 项满足<==>则存在真值指派使 3SAT 所有项满足
2. 存在真值指派使 3SAT 项满足<==>则存在真值指派使 SAT 所有项满足

