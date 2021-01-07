# X3C
该问题的全称为 eXact Cover (by 3-sets)  problem

[3DM](3dm.html) 问题存在一个更一般的形式，即不要求三元素集合 $M$ 中的元素来自三个互不重复的集合，而是都在同一个集合中。



**实例:** 集合 $S$，$|S|=3q$，以及 $S$ 的三元素子集的集合 $C$


**询问:** $C$ 是否包含有一个严格覆盖 $C^{\prime} \subseteq C,$ 使得 $|C^{\prime}|=q$，且 $C^{\prime}$ 中没有任何两个三元组有相同分量。即 $C'$ 中的所有元素恰好只在 $S$ 中出现了一次。



## NPC 证明
该问题的证明非常容易，因为 [3DM](3dm.html) 问题中的每个实例，都可以看成是 X3C 问题的实例。

对 3DM 实例 $W,X,Y,M \subseteq W \times X \times Y$，构造 X3C 实例为 $S=W\cup X\cup Y, C=M$。

3DM 实例 M 中存在完美对集，当且仅当 X3C 实例 C 中存在 S 的严格覆盖。问题得证。


> PS: [issue#7](https://github.com/sailist/AdAlgo/issues/7) 如果 X3C 存在严格覆盖，只需要把严格覆盖的所有元素的第一个分量放到 W，第二个分量放到 X，第三个分量放到 Y 即可

