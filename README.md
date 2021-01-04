# 更新日志

该部份 7 天后删除

 - 2021年1月1日：补充了归并排序复杂度证明 $N$ 为奇数时的讨论，补充了假设法证明复杂度的方法
 - fix issue [#3](https://github.com/sailist/AdAlgo/issues/3)：图灵归约
 - fix issue [#4](https://github.com/sailist/AdAlgo/issues/4)：X3C-Y
 - fix issue [#5](https://github.com/sailist/AdAlgo/issues/5):X3C-Y
 - fix issue [#6](https://github.com/sailist/AdAlgo/issues/6)：VC


# 高级算法

点此进入：[学习链接](https://sailist.github.io/AdAlgo/)（下方link因为部署需要无法直接查看）




## 图论/离散基础

 - [平面图](GraphTheory/1.html)
 - [哈密顿图](GraphTheory/2.html)
 - [独立集](GraphTheory/3.html)
 - [对集/匹配（matching）](GraphTheory/4.html)
 - [补图](GraphTheory/5.html)
 - [二分图](GraphTheory/bg.html)


## 算法分析设计

该部份比较简单，因此不做详细介绍，仅提供一个目录和部份知识点。
 
 - 复杂度分析
 - 分治
   - [归并算法](algo/1.html)
 - 贪心
 - 动规
   - 划分问题
 - 回溯
 - 局搜


## 图灵机与P/NP/NPC
 - [图灵机](./turing/1.html)
   - [确定型图灵机与非确定性图灵机](./turing/2.html)
   - [神谕图灵机](./turing/3.html)
 - [问题形式](./turing/prob.html)
 - [P/NP/NPC/NPH](./turing/4.html)
 - [多项式归约和图灵归约](turing/5.html)
## NPC 问题证明（按照归约顺序排序）

> 列表项中带有 `未完成` 前缀的问题只描述了问题，没有说明具体证明过程；带有 `完成` 前缀的问题描述了问题和核心解决思路，但省略了具体证明过程的；没有符号的问题同时包含了问题和具体证明过程，其中部份额外附注了核心思路。（下同）

 - [x] [SAT（布尔可满足性问题，Cook定理）](doc/sat.html)

---

 - [ ] [3DM（三对集问题）](doc/3dm.html)
   - [X3C](doc/x3c.html)
     - [X3C-Y](doc/3.html)
     - [最小集合覆盖问题](doc/mc.html)
   - [划分三角形问题](doc/partri.html)
   <!-- - *最小测试集问题 -->
 - [3SAT](doc/3sat.html)
   - [x] [VC（顶点覆盖问题）](doc/vc.html)
     - [独立集问题](doc/ivs.html)
       - [团问题](doc/clique.html)
         - [子图同构问题](doc/sgi.html)
         - [最小迟序排工问题](doc/mds.html)
 - [ ] [HC（哈密顿回路问题）](doc/hc.html)
   - [TSP（货郎问题）](doc/tsp.html)
 - [划分问题](doc/par.html)
   - [广义划分问题归约](doc/2.html)
   - [背包问题](doc/knapsack.html)
   - [多任务排工问题](doc/mts.html)
   - [区间排工问题](doc/swi.html)


## NPC 问题证明（按照证明方法排序）

 - 限制技术
   - [最小集合覆盖问题](doc/mc.html)
   - [子图同构问题](doc/sgi.html)
   - [背包问题](doc/knapsack.html)
   - [多任务排工问题](doc/mts.html)
 - 局部替换技术
   - [划分三角形问题](doc/partri.html)
   - [区间排工问题](doc/swi.html)
   - *最小测试集问题
   - *总体计算问题
 - 分支设计技术
   - [最小迟序排工问题](doc/mds.html)
   - .........

## NPC 问题证明（按照证明难度排序）

以下为分级后的题目难度，可能略有出入：

 - 0分
   - [X3C](doc/x3c.html)
   - [最小集合覆盖问题](doc/mc.html)
   - [独立集问题](doc/ivs.html)
   - [团问题](doc/clique.html)
   - [子图同构问题](doc/sgi.html)
   - [背包问题](doc/knapsack.html)
   - [多任务排工问题](doc/mts.html)
 - 1分
   - [广义划分问题归约](doc/2.html)
   - [区间排工问题](doc/swi.html)
 - 2分
   - [X3C-Y](doc/3.html)
   - [最小迟序排工问题](doc/mds.html)
   - [TSP（货郎问题）](doc/tsp.html)
 - 3分
   - [划分三角形问题](doc/partri.html)
   - [3SAT](doc/3sat.html)
   - [x] [VC（顶点覆盖问题）](doc/vc.html)
   - [划分问题](doc/par.html)
   - [*顶点度不超过4的图的三着色](doc/4gcp.html)
   - [ ] [*平面图三着色](doc/pgcp.html)
 - 4分
   - [x] [SAT（布尔可满足性问题，Cook定理）](doc/sat.html)
   - [ ] [3DM（三对集问题）](doc/3dm.html)
   - [ ] [HC（哈密顿回路问题）](doc/hc.html)
 - 5分
   - ...


难度分级按照 0-5 分评级：
 - 0分：**绝对无任何**难度的，一般由等价问题直接归约，只需要理解相关基础概念的问题。
 - 1分：**非绝对无**难度的，不能说一点难度没有，但也不能认为有多少难度，仅能依靠非0分的状态在坐标中定位，这种暧昧的状态被定为 1分，一般由有限步易得条件推导得到。
 - 2分：有难度的**最低值**，但无法对其强弱进行判定，有难度的最低测度。一般是证明存在一定篇幅，但相对理解可以通过举例较为容易的理解的归约。
 - 3分：**很标准**的难，一般是需要大段描述，且中间穿插多个定理，但推演逻辑相对单一线性，且能够通过更简单的描述理解思想的归约。
 - 4分：**标准之上**的难，缺少可以可视化的例子，需要引入许多的符号、公式、定理，只能通过硬核的推导来结束证明。
 - 5分：**具有侵略性**的难。目前仍然未被证明的难题。这暂时不会出现在本项目中。

> 该评级策略参照某定标法略做更改而来，具体链接已经找不到了。个人认为这是主观评分的一个非常棒的标准。

## 其他
 - [ ] [2SAT 问题](doc/2sat.html)
 - [图着色问题](doc/gcp.html)
   - [顶点度不超过4的图的三着色](doc/4gcp.html)
   - [ ] [平面图三着色](doc/pgcp.html)

## 近似算法
 - [近似算法基础](approx/approx.html)
 - [存储最多程序问题](approx/smsp.html)
 - [背包问题贪心策略](doc/knapsack.html)
 - [MST-MM](approx/mstmm.html)


# Reference
 - 感谢姜海涛老师的精彩讲解
 - [《算法设计与分析》，朱大铭,马绍汉, 高等教育出版社-nuuc](https://pan.baidu.com/s/19Uhhbp88ZCE2RLNj8Q_M-w)

