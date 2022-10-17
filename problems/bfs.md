# 宽度优先搜索（BFS）：面试中最常考的

## 基础知识

常见的BFS用来解决什么问题？
（1）简单图（有向无向皆可）的最短路径长度，注意是长度而不是具体的路径
（2）拓扑排序 
（3）遍历一个图（或者树）

BFS基本模板：

- 主要分为需要记录层数或者不需要记录层数两类题
- 多数情况下时间复杂度空间复杂度都是O（N+M），N为节点个数，M为边的个数
- 基于树的BFS：不需要专门一个set来记录访问过的节点

## 练习
- [x] Leetcode 102. 二叉树的层序遍历（★★）(👍👍👍)
- [ ] Leetcode 103 Binary Tree Zigzag Level Order Traversal
- [ ] Leetcode 297 Serialize and Deserialize Binary Tree （很好的BFS和双指针结合的题）



- 基于图的BFS：（一般需要一个set来记录访问过的节点）
- - Leetcode 200. Number of Islands
  - Leetcode 133. Clone Graph
  - Leetcode 127. Word Ladder
  - Leetcode 490. The Maze
  - Leetcode 323. Connected Component in Undirected Graph
  - Leetcode 130. Surrounded Regions
  - Leetcode 752. Open the Lock
  - Leetcode 815. Bus Routes
  - Leetcode 1091. Shortest Path in Binary Matrix
  - Leetcode 542. 01 Matrix
  - Leetcode 1293. Shortest Path in a Grid with Obstacles Elimination
  - Leetcode 417. Pacific Atlantic Water Flow

## 拓扑排序

- 根据依赖关系，构建邻接表、入度数组。把入度为零的结点加入待处理队列中。
- 从待处理队列中弹出一个结点，根据邻接表，减小依赖它的结点的入度。
- 如果入度变为 0， 将该结点加入到待处理队列中，重复第 2 步。
- 直至待处理队列长度为零 0，得到一个拓扑排序。如果还有结点的入度大于 0，说明图中存在环。

## 练习

- [x] Leetcode 207. 课程表（★★）(👍👍👍)
- [ ] Leetcode 444 Sequence Reconstruction
- [ ] Leetcode 269 Alien Dictionary
- [ ] Leetcode 310 Minimum Height Trees
- [ ] Leetcode 366 Find Leaves of Binary Tree
