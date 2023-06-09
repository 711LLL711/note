# 图
## 图的基本概念
有向图、无向图、度、简单图、多重图  
### 握手定理、顶点与边的相互关系
> 无向图--边的数目是顶点个数的两倍  

>定理：一定有偶数个度为奇数的顶点  

> 有向图中,入度=出度=边数  
## 图的类型  
完全图K~n~、轮图  W~n~、圈图C~n~、n立方图Q~n~  
### 二分图（偶图）
1. 着色法判断二分图
2. 完全二分图K~m,n~
   #### 匹配问题
   **霍尔婚姻定理**
   > 二分图中，V1任何子集A,它的邻居（在V2中对应的那个子集B）都大于等于子集A本身
3. 定理：一个图是二分图，当且仅当它不包含奇数长度的回路
## 由旧图构造新图
1. 子图、真子图
>A subgraph is a graph all of whose points and lines are contained in a larger graph. 
2. 生成子图、导出子图  
- An induced subgraph is another graph, formed from a subset of the vertices of the graph and all of the edges (from the original graph) connecting pairs of vertices in that subset.  
- A spanning subgraph is a subgraph that contains all the vertices of the original graph.
## 图的表示
1. 图示法  
2. 邻接表
3. 关联矩阵  
4. 邻接矩阵  
## ⭐图同构
**图同构的必要条件**   
边、顶点的数目相同，对应顶点的度相同,相同度对应的顶点关联的情况也一定相同  
两个图中由度为x的顶点及它们中间的边构成的子图也一定同构
## 通路
1. 通路、连通  
2. 连通分支--极大连通子图  
>  ⭐经常考，简单回路（E>=V）与树（是一种极小连通子图E=V-1）
1. 割点、割边
点割集：删除点割集中的所有点，图不再连通
边割集：删除边割集中的所有边，图不再连通
2. 连通度(边连通度,点连通度)
3. 强连通、弱连通(基图连通)
4. 由邻接矩阵计算顶点之间的通路数
   $A^n^$（邻接矩阵的n次幂）
5. 欧拉通路与欧拉回路
   ### 判断欧拉回路
   > 连通多重图有欧拉回路当且仅当所有顶点的度都是偶数
   ### 判断有欧拉通路但无欧拉回路
   > 连通多重图有欧拉通路当且仅当有且仅有两个顶点的度是奇数
6. 哈密顿回路
   ### 哈密顿回路的充分条件
   > 狄拉克定理：n个顶点的简单图，如果每个顶点的度都大于等于n/2，则这个图一定有哈密顿回路
   > 欧尔定理：n个顶点的简单图，如果对于任意两个不相邻的顶点，它们的度之和都大于等于n，则这个图一定有哈密顿回路
   ### 一些简单的结论判断不存在哈密顿回路
   1. 有度为1的顶点
   2. 若有度为2的顶点，则关联的两条边属于任意一条哈密顿回路
   3. 注意当构造哈密顿回路且回路已经经过某一个顶点，这个顶点其他关联的边都不用再考虑
   4. 有奇数个顶点的二分图没有哈密尔顿回路
7.  最短通路算法
    ### Dijkstra算法
    >原理：设置起点A，首先先将与A相连的点的距离设为这个值，不相连的设为无穷，每次添加新的顶点B，判断所有与该结点直接相邻的结点C，如果新的顶点B作为中间节点使C从A到节点的距离减小，更新节点C的距离
    ### Floyd算法
    > 原理：先把所有顶点加上，考虑在两点之间插入一个顶点会不会使路径变短，如果会则更新最短路径

## 平面图
### ⭐欧拉公式
> 设G是一个连通的平面图，V、E、F分别是G的顶点数、边数、面数，则有V-E+F=2
> 非连通平面图--：连通分支数=顶点数-边数+面数-1
### 利用欧拉公式判断平面图
> 若连通平面简单图图顶点数v>=3,则E<=3V-6
> 若连通平面简单图图顶点数v>=3,没有长度为3的回路，则E<=2V-4
> 若连通平面简单图，则有度不超过5的顶点
### ⭐库拉图斯基定理判断平面图
> 一个图是非平面图当且仅当它有一个子图同胚于K~3,3~或K~5~的

>如何找到K~3,3~或K~5~的子图❓：  
>1. 任取一个顶点，将它的邻居分成两个集合，如果两个集合中的顶点之间没有边，则找到了K~3,3~的子图
>2. 五个顶点之间都互相有边，则找到了K~5~的子图
### 着色问题、着色数
> 四色定理：任何平面图都可以用四种颜色着色，使得任何两个相邻的区域颜色不同  
特殊的图的着色数
1. K~n~的着色数为2
2. K~m,n~的着色数为2
3. C~n~的着色数为3(n>=3且n奇数)，=2(n>=4且n偶数)

对于任意无向图G，均有着色数<=最大度+1  
布鲁克斯定理：对于任意无向图G，均有着色数<=最大度，除非G是完全图或奇圈图