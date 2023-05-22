# 关系relation
> for specific concept,see [wikipedia](https://en.wikipedia.org/wiki/Relation_(mathematics))
## 二元关系的定义
A->B
什么是定义在集合上的关系？
## 关系的性质
1. 自反性Reflexive  
for all x ∈ X, xRx.
1. 传递性Transitive  
for all x, y, z ∈ X, if xRy and yRz then xRz. 
1. 对称性Symmetric  
for all x, y ∈ X, if xRy then yRx. For example  
1. 反对称性Antisymmetric  
for all x, y ∈ X, if xRy and yRx then x = y.  
## 逆关系、空关系
1. 逆关系联系反函数
2. Empty relation
    E = ∅;
## 关系的组合
与集合的组合一致
## 关系的合成、关系的幂
## n元关系、数据库
## 关系的表示
用矩阵表示关系    
从矩阵图看关系的性质  
用图表示关系  
从图看关系的性质  
## 关系的运算
布尔运算交和并、布尔积
## 求关系的闭包
1. 对称闭包、自反闭包
添加缺失的关系组合   
1. Warshell算法求传递闭包
   >一步步允许新的点k作为内点，如果有ik ,kj传递，那么ij传递
   > 最后的传递闭包就是$W^n$
## 等价关系
1. 等价关系是**自反对称传递**的
2. 等价类
3. 等价关系的划分
## 偏序、全序、良序、hase图
1. 偏序关系
> 自反、传递、反对称
1. 全序
> 偏序+集合中每对元素都是可比的
1. 良序
> 全序+每个非空子集都有最小元素
1. hase图
- 	背景：在有穷偏序集中，有些边是必须存在的，不需要在图中表示出来，可以按步骤进行简化，得到哈塞图
- 步骤
    1. 去掉自反边
    2. 去掉传递边
    3. 去掉反对称边
    4. 去掉不可达边
    5. 去掉不可达点
1. 极大元极小元、最大元最小元、格、上界下界、拓扑排序