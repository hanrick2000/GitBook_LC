# 5. DFS

## 分治和遍历法的联系和区别

### 联系

分治和遍历是常见的递归的方法

### 区别

分治：先让左右子树去解决同样的问题，然后得到结果之后，再整合为整棵树的结果。

遍历：通过前序/中序/后序的某种遍历，游走整棵树，通过一个全局变量或者传递的参数来记录这个过程中所遇到的点和需要计算的结果。

从程序实现角度，分治法的递归函数通常有一个`返回值`，遍历法通常没有。

## 搜索，动规和二叉树的时间复杂度计算

搜索的时间复杂度：`O(答案总数 * 构造每个答案的时间)`  
举例：Subsets问题，求所有的子集。子集个数一共 2^n，每个集合的平均长度是 O\(n\) 的，所以时间复杂度为 O\(n \* 2^n\)，同理 Permutations 问题的时间复杂度为：O\(n \* n!\)

动态规划的时间复杂度：`O(状态总数 * 计算每个状态的时间复杂度)`  
举例：triangle，数字三角形的最短路径，状态总数约 O\(n^2\) 个，计算每个状态的时间复杂度为 O\(1\)——就是求一下 min。所以总的时间复杂度为 O\(n^2\)

用分治法解决二叉树问题的时间复杂度：`O(二叉树节点个数 * 每个节点的计算时间)`  
举例：二叉树最大深度。二叉树节点个数为 N，每个节点上的计算时间为 O\(1\)。总的时间复杂度为 O\(N\)

