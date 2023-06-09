# 十大排序算法
* [冒泡排序--bubble_sort](#冒泡排序)
* [选择排序--select_sort](#选择排序)
* [插入排序--insert_sort](#插入排序)
* [希尔排序--shell_sort](#希尔排序)
* [归并排序--merge_sort](#归并排序)
* [快速排序--quick_sort](#快速排序)
* [堆排序--heap_sort](#堆排序)
* [计数排序--counting_sort](#计数排序)
* [桶排序--bucket_sort](#桶排序)
* [基数排序--radix_sort](#基数排序)

## 时间复杂度
![时间复杂度](sort.png)
❗Not sure about time plexity of shell sort
> 希尔排序时间复杂度是 O(n^(1.3-2))，空间复杂度为常数阶 O(1)。希尔排序没有时间复杂度为 O(n(logn)) 的快速排序算法快 ，  
> 因此对中等大小规模表现良好，但对规模非常大的数据排序不是最优选择，总之比一般 O(n^2 ) 复杂度的算法快得多。---from cainiao tutorial  

> For many practical variants, determining their time complexity remains an open problem. ---from wikipedia
## 思路和C语言代码实现
to do...

# 查找算法

* [顺序查找](#顺序查找)
* [二分查找](#二分查找)
* [分块查找](#分块查找)
* [哈希查找](#哈希查找)
* [二叉排序树查找](#二叉排序树查找)


|name|time|ASL|strength|weakness|
|:---|:---|:---|:---|:---|
|顺序查找|O(n)|$(n+1)/2$|简单|ASL高|
|二分查找|O(logn)|$\approx\log_2(n+1)$|..|必须有序|
|分块查找|..|$ASL_(索引表查找的)+ASL_(块内查找的)\approx log_2(n/s+1)+s/2$|无需有序|..|

## 二叉搜索树
### 二叉搜索树的定义
所有节点的左子树小于根节点，右子树大于根节点，且左右子树也是二叉搜索树。中序遍历就是从小到大  

### 二叉搜索树的查找
小于该节点搜左子树  
大于搜右子树
### 二叉搜索树的插入
插入一定在叶子节点上
### 二叉搜索树的删除
三种情况：  
* 度为0
* 度为1
* 度为2
### 平衡二叉搜索树
平衡因子的概念--左子树高度-右子树高度，>2就是不平衡  
如何平衡化？

## 散列表（哈希表）查找
### 散列表基本思想
---元素的存储位置与关键字有对应关系   
---哈希函数是桥梁
### 散列表的构造
1. 直接定址法
   取关键字或关键字的某个线性函数值为散列地址。即H(key)=key或H(key) = a·key + b，其中a和b为常数（这种散列函数叫做自身函数）。
2. 除留余数法⭐
    f(key) = key mod p (p≤m)，m为散列表长。这种方法不仅可以对关键字直接取模，也可在折叠、平方取中后再取模。根据经验，若散列表表长为m，通常p为小于或等于表长（最好接近m）的最小质数，可以更好的减小冲突。
3. [其他方法](create.md)  
下面这些因素可以作为选取散列函数的参考：（1）计算散列地址所需的时间；（2）关键字长度；（3）散列表大小；（4）关键字的分布情况；（5）查找记录的频率。

### 散列表解决冲突的方法
#### 同义词
根据哈希函数，不同的关键词可能映射到相同的存储位置，称为互为同义词，产生冲突
#### 方法小结
1. 开放定址法
   - 线性探测
   - 二次探测
   - 伪随机探测
2. 拉链法
   在存储的位置拉出一个链表来存所有的同义词
3. 再散链法、公共溢出区法

### 时间效率分析
![ASL](ASL.bmp)




  