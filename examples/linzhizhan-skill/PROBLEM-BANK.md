# 林知栈 · 经典算法题库

> 200+ 道精选题，按 pattern × 难度组织。每道题标注核心考点和前置知识。
> 用途：林知栈根据学习者的水平和目标，从题库中精准提取练习题。

---

## 使用说明

林知栈在推荐题目时遵循以下原则：

1. **先识别 pattern，再选题目**：不按题号顺序刷，按 pattern 集中突破
2. **渐进难度**：每个 pattern 内 Easy → Medium → Hard
3. **前置依赖**：推荐题目前检查学习者是否掌握了前置知识
4. **变体训练**：同一 pattern 下推荐 2-3 道变体，训练迁移能力
5. **定期回顾**：推荐「间隔重复」——学完 pattern B 后回头做 pattern A 的 Hard 题

### 难度标记

- 🟢 Easy：入门，建立直觉
- 🟡 Medium：核心，训练 pattern 识别
- 🔴 Hard：进阶，综合运用 + 优化

### 来源标记

- `NC` = NeetCode / Blind 75 / NeetCode 150
- `SP` = Sean Prashad LeetCode Patterns
- `AM` = AlgoMonster
- `CF` = 代码随想录 / Carl
- `LD` = labuladong
- `AC` = AcWing / yxc
- `LB` = 刘宇波 bobo
- `LC` = 洛谷

---

## 1. 数组与哈希 (Array & Hashing)

**核心模型**：哈希表 = O(1) 的查找。当你需要「快速判断某个元素是否存在」或「统计频率」时，想到哈希。

**前置知识**：数组遍历、哈希表基本操作

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 1 | Two Sum | 🟢 | 哈希查找补数 | NC, SP, CF, LD |
| 2 | 217 | Contains Duplicate | 🟢 | 集合去重 | NC, SP, CF |
| 3 | 242 | Valid Anagram | 🟢 | 频率统计 | NC, SP, CF, LD |
| 4 | 49 | Group Anagrams | 🟡 | 排序后哈希分组 | NC, SP, CF, LD |
| 5 | 347 | Top K Frequent Elements | 🟡 | 频率统计 + 桶排序/堆 | NC, SP, CF, LD |
| 6 | 238 | Product of Array Except Self | 🟡 | 前缀积/后缀积 | NC, SP, CF, LD |
| 7 | 128 | Longest Consecutive Sequence | 🟡 | 哈希集合 + 连续序列 | NC, SP, CF, LD |
| 8 | 271 | Encode and Decode Strings | 🟡 | 编码设计 | NC, SP |
| 9 | 146 | LRU Cache | 🟡 | 哈希 + 双向链表 | NC, SP, CF, LD |
| 10 | 380 | Insert Delete GetRandom O(1) | 🟡 | 哈希 + 数组 | NC, SP |
| 11 | 36 | Valid Sudoku | 🟡 | 行/列/宫哈希检查 | NC, SP, CF |
| 12 | 560 | Subarray Sum Equals K | 🟡 | 前缀和 + 哈希 | CF, AC |
| 13 | 41 | First Missing Positive | 🔴 | 原地哈希（下标映射） | NC, SP, LD |

---

## 2. 双指针 (Two Pointers)

**核心模型**：两个指针在有序结构上相向/同向移动，每次移动都能排除一部分搜索空间。

**前置知识**：数组/链表遍历、排序

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 125 | Valid Palindrome | 🟢 | 左右指针过滤字符 | NC, SP, CF |
| 2 | 680 | Valid Palindrome II | 🟢 | 允许删除一个字符 | SP |
| 3 | 15 | 3Sum | 🟡 | 排序 + 双指针去重 | NC, SP, CF, LD |
| 4 | 11 | Container With Most Water | 🟡 | 贪心收缩 | NC, SP, CF, LD |
| 5 | 42 | Trapping Rain Water | 🔴 | 双指针/单调栈 | NC, SP, CF, LD |
| 6 | 167 | Two Sum II - Input Array Is Sorted | 🟢 | 有序数组双指针 | NC, SP, CF |
| 7 | 881 | Boats to Save People | 🟡 | 贪心 + 双指针 | SP |
| 8 | 75 | Sort Colors | 🟡 | 三指针（荷兰国旗） | NC, SP, CF, LD |
| 9 | 283 | Move Zeroes | 🟢 | 快慢指针 | NC, CF |
| 10 | 844 | Backspace String Compare | 🟡 | 逆序双指针 | SP |
| 11 | 977 | Squares of a Sorted Array | 🟢 | 逆序双指针合并 | CF |
| 12 | 16 | 3Sum Closest | 🟡 | 排序 + 双指针 + 最接近 | SP |

---

## 3. 滑动窗口 (Sliding Window)

**核心模型**：维护一个「窗口」，通过移动左右边界来寻找最优解。窗口内的状态用哈希表/计数器维护。

**前置知识**：双指针、哈希表

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 121 | Best Time to Buy and Sell Stock | 🟢 | 单次交易最大利润 | NC, SP, CF, LD |
| 2 | 3 | Longest Substring Without Repeating Characters | 🟡 | 字符哈希 + 窗口收缩 | NC, SP, CF, LD |
| 3 | 424 | Longest Repeating Character Replacement | 🟡 | 窗口内最多替换k个 | NC, SP, CF, LD |
| 4 | 567 | Permutation in String | 🟡 | 固定窗口 + 频率匹配 | NC, SP, CF, LD |
| 5 | 76 | Minimum Window Substring | 🔴 | 变长窗口 + 覆盖条件 | NC, SP, CF, LD |
| 6 | 239 | Sliding Window Maximum | 🔴 | 单调队列 + 滑窗 | NC, SP, CF, LD |
| 7 | 209 | Minimum Size Subarray Sum | 🟡 | 最短满足子数组 | SP, CF |
| 8 | 438 | Find All Anagrams in a String | 🟡 | 固定窗口 + 频率匹配 | NC, SP, CF |
| 9 | 30 | Substring with Concatenation of All Words | 🔴 | 多词拼接窗口 | NC, SP |
| 10 | 904 | Fruit Into Baskets | 🟡 | 最多两种元素的窗口 | SP |
| 11 | 1004 | Max Consecutive Ones III | 🟡 | 最多翻转k个0 | SP, CF |
| 12 | 187 | Repeated DNA Sequences | 🟡 | 固定10字符窗口 | SP |

---

## 4. 栈 (Stack)

**核心模型**：后进先出。用于匹配、嵌套、单调性维护。单调栈 = 在 O(n) 内找到每个元素的「下一个更大/更小元素」。

**前置知识**：栈的基本操作

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 20 | Valid Parentheses | 🟢 | 括号匹配 | NC, SP, CF, LD |
| 2 | 155 | Min Stack | 🟡 | 辅助栈维护最小值 | NC, SP, CF |
| 3 | 150 | Evaluate Reverse Polish Notation | 🟡 | 后缀表达式求值 | NC, SP, CF |
| 4 | 739 | Daily Temperatures | 🟡 | 单调递减栈 | NC, SP, CF, LD |
| 5 | 853 | Car Fleet | 🟡 | 排序 + 栈 | SP |
| 6 | 84 | Largest Rectangle in Histogram | 🔴 | 单调递增栈 | NC, SP, CF, LD |
| 7 | 71 | Simplify Path | 🟡 | 路径解析栈 | SP |
| 8 | 224 | Basic Calculator | 🔴 | 带括号的表达式求值 | NC, SP |
| 9 | 394 | Decode String | 🟡 | 嵌套解码栈 | NC, SP, CF |
| 10 | 946 | Validate Stack Sequences | 🟡 | 模拟栈操作 | SP |
| 11 | 496 | Next Greater Element I | 🟢 | 单调栈入门 | SP, CF |
| 12 | 503 | Next Greater Element II | 🟡 | 循环数组单调栈 | CF |

---

## 5. 二分查找 (Binary Search)

**核心模型**：在有序（或单调）空间中，每次排除一半搜索空间。关键是定义清楚「搜索空间」和「判断条件」。

**前置知识**：数组、循环/递归

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 704 | Binary Search | 🟢 | 标准二分 | NC, SP, CF |
| 2 | 74 | Search a 2D Matrix | 🟡 | 矩阵二分 | NC, SP, CF |
| 3 | 33 | Search in Rotated Sorted Array | 🟡 | 旋转数组二分 | NC, SP, CF, LD |
| 4 | 153 | Find Minimum in Rotated Sorted Array | 🟡 | 旋转数组找最小值 | NC, SP, CF, LD |
| 5 | 34 | Find First and Last Position of Element | 🟡 | 左右边界二分 | NC, SP, CF, LD |
| 6 | 875 | Koko Eating Bananas | 🟡 | 二分答案 | NC, SP, CF, LD |
| 7 | 162 | Find Peak Element | 🟡 | 局部二分 | NC, SP, CF |
| 8 | 4 | Median of Two Sorted Arrays | 🔴 | 双数组二分 | NC, SP, CF, LD |
| 9 | 981 | Time Based Key-Value Store | 🟡 | 时间戳二分 | NC, SP |
| 10 | 702 | Search in a Sorted Array of Unknown Size | 🟡 | 未知长度二分 | SP |
| 11 | 69 | Sqrt(x) | 🟢 | 整数二分 | CF |
| 12 | 1011 | Capacity To Ship Packages Within D Days | 🟡 | 二分答案 + 贪心验证 | SP, CF |
| 13 | 1283 | Find the Smallest Divisor Given a Threshold | 🟡 | 二分答案 | CF |

---

## 6. 链表 (Linked List)

**核心模型**：指针操作。核心技巧：dummy 节点、快慢指针、反转/合并/拆分。

**前置知识**：指针/引用、链表结构

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 206 | Reverse Linked List | 🟢 | 迭代/递归反转 | NC, SP, CF, LD |
| 2 | 21 | Merge Two Sorted Lists | 🟢 | 合并有序链表 | NC, SP, CF, LD |
| 3 | 141 | Linked List Cycle | 🟢 | 快慢指针判环 | NC, SP, CF, LD |
| 4 | 142 | Linked List Cycle II | 🟡 | 环入口检测 | NC, SP, CF, LD |
| 5 | 287 | Find the Duplicate Number | 🟡 | 快慢指针（数组当链表） | NC, SP, CF, LD |
| 6 | 876 | Middle of the Linked List | 🟢 | 快慢指针找中点 | NC, SP, CF |
| 7 | 19 | Remove Nth Node From End | 🟡 | 快慢指针间隔n | NC, SP, CF, LD |
| 8 | 143 | Reorder List | 🟡 | 找中点 + 反转 + 合并 | NC, SP, CF |
| 9 | 23 | Merge k Sorted Lists | 🔴 | 分治合并 / 最小堆 | NC, SP, CF, LD |
| 10 | 25 | Reverse Nodes in k-Group | 🔴 | 分组反转 | NC, SP, CF, LD |
| 11 | 138 | Copy List with Random Pointer | 🟡 | 哈希/原地复制 | NC, SP, CF |
| 12 | 2 | Add Two Numbers | 🟡 | 链表模拟加法 | NC, SP, CF, LD |
| 13 | 146 | LRU Cache | 🟡 | 哈希 + 双向链表 | NC, SP, CF, LD |

---

## 7. 树 (Trees)

**核心模型**：递归结构。树的大多数问题都可以用递归解决：定义好「当前节点做什么」和「子问题返回什么」。

**前置知识**：递归、树的遍历（前/中/后序、层序）

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 226 | Invert Binary Tree | 🟢 | 递归翻转 | NC, SP, CF, LD |
| 2 | 104 | Maximum Depth of Binary Tree | 🟢 | 递归求深度 | NC, SP, CF, LD |
| 3 | 100 | Same Tree | 🟢 | 递归比较 | NC, SP, CF |
| 4 | 572 | Subtree of Another Tree | 🟢 | 子树匹配 | NC, SP, CF |
| 5 | 236 | Lowest Common Ancestor of a Binary Tree | 🟡 | LCA 递归 | NC, SP, CF, LD |
| 6 | 102 | Binary Tree Level Order Traversal | 🟡 | BFS 层序遍历 | NC, SP, CF, LD |
| 7 | 98 | Validate Binary Search Tree | 🟡 | BST 验证（上下界） | NC, SP, CF, LD |
| 8 | 230 | Kth Smallest Element in a BST | 🟡 | 中序遍历第k个 | NC, SP, CF |
| 9 | 105 | Construct Binary Tree from Preorder and Inorder | 🟡 | 前序+中序重建 | NC, SP, CF, LD |
| 10 | 124 | Binary Tree Maximum Path Sum | 🔴 | 路径和（全局变量） | NC, SP, CF, LD |
| 11 | 297 | Serialize and Deserialize Binary Tree | 🔴 | 序列化/反序列化 | NC, SP, CF, LD |
| 12 | 543 | Diameter of Binary Tree | 🟢 | 求直径（最长路径） | NC, SP, CF |
| 13 | 114 | Flatten Binary Tree to Linked List | 🟡 | 原地展开 | NC, SP, CF |
| 14 | 437 | Path Sum III | 🟡 | 前缀和 + 递归 | NC, SP, CF |
| 15 | 110 | Balanced Binary Tree | 🟢 | 平衡判断 | NC, SP, CF |
| 16 | 662 | Maximum Width of Binary Tree | 🟡 | BFS + 下标索引 | SP |

---

## 8. 前缀树 (Trie)

**核心模型**：字符级别的树形结构。用于「前缀匹配」「自动补全」「词频统计」。

**前置知识**：树、递归

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 208 | Implement Trie (Prefix Tree) | 🟡 | Trie 基本实现 | NC, SP, CF, LD |
| 2 | 211 | Design Add and Search Words Data Structure | 🟡 | 通配符匹配（DFS） | NC, SP, CF, LD |
| 3 | 212 | Word Search II | 🔴 | Trie + 回溯 | NC, SP, CF, LD |
| 4 | 648 | Replace Words | 🟡 | 前缀替换 | SP |
| 5 | 677 | Map Sum Pairs | 🟡 | Trie 存储值 | SP |
| 6 | 14 | Longest Common Prefix | 🟢 | 纵向扫描 / Trie | CF |
| 7 | 386 | Lexicographical Numbers | 🟡 | Trie/DFS 字典序 | SP |

---

## 9. 堆 / 优先队列 (Heap / Priority Queue)

**核心模型**：快速获取最大/最小值。用于 Top-K 问题、合并有序流、调度问题。

**前置知识**：完全二叉树、数组实现堆

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 703 | Kth Largest Element in a Stream | 🟢 | 最小堆维护Top-K | NC, SP, CF |
| 2 | 1046 | Last Stone Weight | 🟢 | 最大堆模拟 | NC, SP, CF |
| 3 | 973 | K Closest Points to Origin | 🟡 | Top-K 堆 | NC, SP, CF |
| 4 | 215 | Kth Largest Element in an Array | 🟡 | 快速选择 / 堆 | NC, SP, CF, LD |
| 5 | 621 | Task Scheduler | 🟡 | 贪心 + 堆 | NC, SP, CF, LD |
| 6 | 355 | Design Twitter | 🟡 | 合并多有序流 | NC, SP, CF |
| 7 | 295 | Find Median from Data Stream | 🔴 | 双堆（大顶堆+小顶堆） | NC, SP, CF, LD |
| 8 | 23 | Merge k Sorted Lists | 🔴 | 多路归并堆 | NC, SP, CF, LD |
| 9 | 767 | Reorganize String | 🟡 | 贪心 + 频率堆 | SP |
| 10 | 1642 | Furthest Building You Can Reach | 🟡 | 贪心 + 堆 | SP |
| 11 | 1834 | Single-Threaded CPU | 🟡 | 事件调度堆 | SP |

---

## 10. 回溯 (Backtracking)

**核心模型**：状态空间树的 DFS。做选择 → 递归 → 撤销选择。关键是「选择列表」和「剪枝条件」。

**前置知识**：递归、树的 DFS

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 78 | Subsets | 🟡 | 子集枚举 | NC, SP, CF, LD |
| 2 | 39 | Combination Sum | 🟡 | 无限选择 + 剪枝 | NC, SP, CF, LD |
| 3 | 46 | Permutations | 🟡 | 全排列 | NC, SP, CF, LD |
| 4 | 90 | Subsets II | 🟡 | 去重子集 | NC, SP, CF, LD |
| 5 | 40 | Combination Sum II | 🟡 | 每个元素用一次 | NC, SP, CF |
| 6 | 47 | Permutations II | 🟡 | 去重全排列 | NC, SP, CF |
| 7 | 79 | Word Search | 🟡 | 网格 DFS + 回溯 | NC, SP, CF |
| 8 | 131 | Palindrome Partitioning | 🟡 | 分割回溯 | NC, SP, CF, LD |
| 9 | 17 | Letter Combinations of a Phone Number | 🟡 | 多选一回溯 | NC, SP, CF |
| 10 | 51 | N-Queens | 🔴 | 经典 N 皇后 | NC, SP, CF, LD |
| 11 | 37 | Sudoku Solver | 🔴 | 约束回溯 | NC, SP |
| 12 | 22 | Generate Parentheses | 🟡 | 括号生成 | NC, SP, CF, LD |
| 13 | 93 | Restore IP Addresses | 🟡 | 分割 + 验证 | CF |
| 14 | 140 | Word Break II | 🔴 | 回溯 + 记忆化 | SP |

---

## 11. 图 (Graphs)

**核心模型**：节点 + 边的关系网络。核心算法：BFS（最短路/层序）、DFS（连通性/拓扑）、Dijkstra（加权最短路）。

**前置知识**：树的遍历、递归、队列/栈

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 200 | Number of Islands | 🟡 | 网格 DFS/BFS 连通分量 | NC, SP, CF, LD |
| 2 | 133 | Clone Graph | 🟡 | BFS/DFS + 哈希复制 | NC, SP, CF, LD |
| 3 | 695 | Max Area of Island | 🟡 | DFS 面积统计 | NC, SP, CF |
| 4 | 417 | Pacific Atlantic Water Flow | 🟡 | 双源 BFS | NC, SP, CF |
| 5 | 130 | Surrounded Regions | 🟡 | 边界 DFS | NC, SP, CF |
| 6 | 994 | Rotting Oranges | 🟡 | 多源 BFS | NC, SP, CF |
| 7 | 207 | Course Schedule | 🟡 | 拓扑排序（入度法/DFS） | NC, SP, CF, LD |
| 8 | 210 | Course Schedule II | 🟡 | 拓扑排序输出顺序 | NC, SP, CF, LD |
| 9 | 684 | Redundant Connection | 🟡 | 并查集 | NC, SP, CF |
| 10 | 323 | Number of Connected Components | 🟡 | 并查集/DFS | SP |
| 11 | 127 | Word Ladder | 🔴 | BFS 最短转换 | NC, SP, CF, LD |
| 12 | 269 | Alien Dictionary | 🔴 | 拓扑排序建图 | NC, SP |
| 13 | 743 | Network Delay Time | 🟡 | Dijkstra | NC, SP, CF, LD |
| 14 | 787 | Cheapest Flights Within K Stops | 🟡 | 带限制最短路 | NC, SP, CF |

---

## 12. 动态规划 · 一维 (1D DP)

**核心模型**：dp[i] = 到第 i 个状态时的最优解。状态转移 = 「选或不选」「取哪个」。

**前置知识**：递归、数组

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 70 | Climbing Stairs | 🟢 | 基础 DP（斐波那契） | NC, SP, CF, LD |
| 2 | 198 | House Robber | 🟡 | 选或不选 | NC, SP, CF, LD |
| 3 | 213 | House Robber II | 🟡 | 环形数组拆分 | NC, SP, CF, LD |
| 4 | 5 | Longest Palindromic Substring | 🟡 | 中心扩展 / 区间DP | NC, SP, CF, LD |
| 5 | 647 | Palindromic Substrings | 🟡 | 中心扩展计数 | NC, SP, CF |
| 6 | 91 | Decode Ways | 🟡 | 分类讨论 DP | NC, SP, CF, LD |
| 7 | 139 | Word Break | 🟡 | 字符串分割 DP | NC, SP, CF, LD |
| 8 | 152 | Maximum Product Subarray | 🟡 | 维护最大/最小值 | NC, SP, CF, LD |
| 9 | 322 | Coin Change | 🟡 | 完全背包 | NC, SP, CF, LD |
| 10 | 300 | Longest Increasing Subsequence | 🟡 | LIS（二分优化） | NC, SP, CF, LD |
| 11 | 1143 | Longest Common Subsequence | 🟡 | LCS 经典 | CF, LD |
| 12 | 416 | Partition Equal Subset Sum | 🟡 | 0-1 背包 | NC, SP, CF, LD |
| 13 | 494 | Target Sum | 🟡 | 0-1 背包变体 | NC, SP, CF |
| 14 | 279 | Perfect Squares | 🟡 | 完全背包 | NC, SP, CF |
| 15 | 1049 | Last Stone Weight II | 🟡 | 0-1 背包（分两堆） | SP |

---

## 13. 动态规划 · 多维 (Multi-Dim DP)

**核心模型**：dp[i][j] = 两个（或多个）维度的状态。常见：字符串匹配、网格路径、区间DP。

**前置知识**：一维 DP

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 62 | Unique Paths | 🟡 | 网格路径计数 | NC, SP, CF, LD |
| 2 | 64 | Minimum Path Sum | 🟡 | 网格最短路径 | NC, SP, CF |
| 3 | 72 | Edit Distance | 🔴 | 字符串编辑 DP | NC, SP, CF, LD |
| 4 | 97 | Interleaving String | 🟡 | 双指针 DP | NC, SP, CF |
| 5 | 115 | Distinct Subsequences | 🔴 | 子序列匹配 DP | NC, SP, CF |
| 6 | 329 | Longest Increasing Path in a Matrix | 🟡 | 记忆化 DFS | NC, SP, CF |
| 7 | 312 | Burst Balloons | 🔴 | 区间 DP | NC, SP, CF, LD |
| 8 | 516 | Longest Palindromic Subsequence | 🟡 | 区间 DP | CF, LD |
| 9 | 10 | Regular Expression Matching | 🔴 | 字符串匹配 DP | NC, SP, CF, LD |
| 10 | 44 | Wildcard Matching | 🔴 | 通配符匹配 DP | NC, SP |
| 11 | 188 | Best Time to Buy and Sell Stock IV | 🔴 | 状态机 DP（k次交易） | NC, SP, CF, LD |
| 12 | 123 | Best Time to Buy and Sell Stock III | 🔴 | 状态机 DP（2次交易） | NC, SP, CF |
| 13 | 309 | Best Time to Buy and Sell Stock with Cooldown | 🟡 | 状态机 DP | NC, SP, CF, LD |
| 14 | 714 | Best Time to Buy and Sell Stock with Transaction Fee | 🟡 | 状态机 DP | NC, SP, CF |

---

## 14. 贪心 (Greedy)

**核心模型**：每一步选局部最优，最终得到全局最优。关键是证明「贪心选择性质」——局部最优不会导致全局更差。

**前置知识**：排序、基本数据结构

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 53 | Maximum Subarray | 🟡 | Kadane 算法 | NC, SP, CF, LD |
| 2 | 55 | Jump Game | 🟡 | 能到达的最远位置 | NC, SP, CF, LD |
| 3 | 45 | Jump Game II | 🟡 | 最少跳跃次数 | NC, SP, CF, LD |
| 4 | 134 | Gas Station | 🟡 | 环形贪心 | NC, SP, CF |
| 5 | 763 | Partition Labels | 🟡 | 区间合并贪心 | NC, SP, CF |
| 6 | 678 | Valid Parenthesis String | 🟡 | 贪心维护范围 | NC, SP |
| 7 | 122 | Best Time to Buy and Sell Stock II | 🟡 | 累加正差值 | NC, SP, CF, LD |
| 8 | 452 | Minimum Number of Arrows to Burst Balloons | 🟡 | 区间贪心 | SP, CF |
| 9 | 435 | Non-overlapping Intervals | 🟡 | 区间调度贪心 | SP, CF |
| 10 | 1899 | Merge Triplets to Form Target Triplet | 🟡 | 贪心筛选 | SP |
| 11 | 135 | Candy | 🔴 | 左右两次扫描 | NC, SP, CF |
| 12 | 632 | Smallest Range Covering Elements from K Lists | 🔴 | 多指针贪心 + 堆 | SP |

---

## 15. 区间 (Intervals)

**核心模型**：区间操作的通用模式——排序后线性扫描。排序键 = 起点或终点，取决于问题类型。

**前置知识**：排序、贪心

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 56 | Merge Intervals | 🟡 | 排序 + 合并重叠 | NC, SP, CF, LD |
| 2 | 57 | Insert Interval | 🟡 | 三段式插入 | NC, SP, CF, LD |
| 3 | 435 | Non-overlapping Intervals | 🟡 | 最大不重叠区间数 | SP, CF |
| 4 | 252 | Meeting Rooms | 🟢 | 判断是否重叠 | NC, SP |
| 5 | 253 | Meeting Rooms II | 🟡 | 最小会议室数 | NC, SP, CF |
| 6 | 1288 | Remove Covered Intervals | 🟡 | 排序 + 覆盖判断 | SP |
| 7 | 986 | Interval List Intersections | 🟡 | 双指针求交集 | NC, SP, CF |
| 8 | 1851 | Minimum Interval to Include Each Query | 🔴 | 扫描线 + 堆 | SP |
| 9 | 218 | The Skyline Problem | 🔴 | 扫描线 + 堆 | NC, SP |
| 10 | 759 | Employee Free Time | 🟡 | 合并求空隙 | SP |

---

## 16. 数学与几何 (Math & Geometry)

**核心模型**：数学直觉 + 几何公式。常见：GCD/LCM、素数筛、坐标几何、矩阵运算。

**前置知识**：基本数学运算

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 48 | Rotate Image | 🟡 | 矩阵旋转（转置+翻转） | NC, SP, CF |
| 2 | 54 | Spiral Matrix | 🟡 | 模拟螺旋遍历 | NC, SP, CF |
| 3 | 73 | Set Matrix Zeroes | 🟡 | 原地标记 | NC, SP, CF |
| 4 | 202 | Happy Number | 🟢 | 快慢指针判循环 | NC, SP, CF |
| 5 | 66 | Plus One | 🟢 | 进位模拟 | CF |
| 6 | 50 | Pow(x, n) | 🟡 | 快速幂 | NC, SP, CF |
| 7 | 2013 | Detect Squares | 🟡 | 坐标计数 | SP |
| 8 | 149 | Max Points on a Line | 🔴 | 斜率哈希 | NC, SP |
| 9 | 9 | Palindrome Number | 🟢 | 数字回文判断 | CF |
| 10 | 13 | Roman to Integer | 🟢 | 规则模拟 | CF |
| 11 | 12 | Integer to Roman | 🟡 | 贪心映射 | CF |
| 12 | 172 | Factorial Trailing Zeroes | 🟡 | 数学分析（5的个数） | SP |

---

## 17. 位运算 (Bit Manipulation)

**核心模型**：利用二进制位的特性做 O(1) 操作。核心：异或（消消乐）、与/或（掩码）、移位（乘除2）。

**前置知识**：二进制表示

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 136 | Single Number | 🟢 | 异或消消乐 | NC, SP, CF |
| 2 | 191 | Number of 1 Bits | 🟢 | n & (n-1) 消最低位 | NC, SP, CF |
| 3 | 338 | Counting Bits | 🟢 | DP + 位运算 | NC, SP, CF |
| 4 | 190 | Reverse Bits | 🟢 | 逐位翻转 | NC, SP, CF |
| 5 | 268 | Missing Number | 🟢 | 异或/求和 | NC, SP, CF |
| 6 | 371 | Sum of Two Integers | 🟡 | 不用加号的加法 | NC, SP |
| 7 | 7 | Reverse Integer | 🟡 | 数字反转 + 溢出检查 | CF |

---

## 18. 高级数据结构 (Advanced Data Structures)

**核心模型**：超越基本数据结构的工具。用于特定场景下的性能优化。

**前置知识**：树、数组、哈希表

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 307 | Range Sum Query - Mutable | 🟡 | 线段树 / 树状数组 | CF, AC |
| 2 | 315 | Count of Smaller Numbers After Self | 🔴 | 归并排序 / 线段树 / BIT | NC, SP, CF |
| 3 | 493 | Reverse Pairs | 🔴 | 归并排序计数 | SP, CF |
| 4 | 729 | My Calendar I | 🟡 | 有序集合 / 线段树 | SP |
| 5 | 1146 | Snapshot Array | 🟡 | 二分 + 快照 | SP |

---

## 19. 设计题 (Design)

**核心模型**：数据结构设计 = 选择合适的底层结构 + 定义操作的时间复杂度目标。

**前置知识**：各种基本数据结构

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 380 | Insert Delete GetRandom O(1) | 🟡 | 哈希 + 数组 | NC, SP |
| 2 | 146 | LRU Cache | 🟡 | 哈希 + 双向链表 | NC, SP, CF, LD |
| 3 | 460 | LFU Cache | 🔴 | 双哈希 + 双向链表 | NC, SP, CF |
| 4 | 295 | Find Median from Data Stream | 🔴 | 双堆 | NC, SP, CF, LD |
| 5 | 297 | Serialize and Deserialize Binary Tree | 🔴 | BFS/DFS 编解码 | NC, SP, CF, LD |
| 6 | 211 | Design Add and Search Words Data Structure | 🟡 | Trie + 通配符 | NC, SP, CF |
| 7 | 355 | Design Twitter | 🟡 | 哈希 + 堆 | NC, SP, CF |
| 8 | 981 | Time Based Key-Value Store | 🟡 | 哈希 + 二分 | NC, SP |

---

## 20. 并查集 (Union-Find)

**核心模型**：处理「连通性」问题——判断两个元素是否在同一集合，合并集合。

**前置知识**：树、递归

| # | 题号 | 题名 | 难度 | 核心考点 | 来源 |
|---|------|------|------|---------|------|
| 1 | 684 | Redundant Connection | 🟡 | 并查集判环 | NC, SP, CF |
| 2 | 323 | Number of Connected Components | 🟡 | 连通分量计数 | SP |
| 3 | 547 | Number of Provinces | 🟡 | 连通分量 | CF |
| 4 | 721 | Accounts Merge | 🟡 | 并查集合并 | NC, SP, CF |
| 5 | 839 | Similar String Groups | 🔴 | 并查集 + 字符串相似性 | SP |
| 6 | 128 | Longest Consecutive Sequence | 🟡 | 并查集/哈希 | NC, SP, CF |

---

## 题库统计

| Pattern | 题目数 | Easy | Medium | Hard |
|---------|--------|------|--------|------|
| 数组与哈希 | 13 | 3 | 9 | 1 |
| 双指针 | 12 | 3 | 8 | 1 |
| 滑动窗口 | 12 | 1 | 8 | 3 |
| 栈 | 12 | 2 | 8 | 2 |
| 二分查找 | 13 | 2 | 10 | 1 |
| 链表 | 13 | 4 | 7 | 2 |
| 树 | 16 | 5 | 9 | 2 |
| 前缀树 | 7 | 1 | 5 | 1 |
| 堆/优先队列 | 11 | 2 | 7 | 2 |
| 回溯 | 14 | 0 | 11 | 3 |
| 图 | 14 | 0 | 11 | 3 |
| 动态规划·一维 | 15 | 1 | 14 | 0 |
| 动态规划·多维 | 14 | 0 | 8 | 6 |
| 贪心 | 12 | 0 | 11 | 1 |
| 区间 | 10 | 1 | 7 | 2 |
| 数学与几何 | 12 | 4 | 7 | 1 |
| 位运算 | 7 | 5 | 2 | 0 |
| 高级数据结构 | 5 | 0 | 3 | 2 |
| 设计题 | 8 | 0 | 4 | 4 |
| 并查集 | 6 | 0 | 5 | 1 |
| **合计** | **225** | **34** | **152** | **39** |

---

## 林知栈的推荐路线

### 面试冲刺路线（4-6周）

按以下顺序突破 pattern，每个 pattern 3-5 天：

```
Week 1: 数组与哈希 → 双指针 → 滑动窗口
Week 2: 栈 → 二分查找 → 链表
Week 3: 树（重点！）→ 前缀树 → 堆
Week 4: 回溯 → 图（BFS/DFS/拓扑排序）
Week 5: 动态规划（一维 → 多维）→ 贪心
Week 6: 区间 → 数学 → 设计题（查漏补缺）
```

### 打基础路线（8-12周）

在面试冲刺路线基础上：
- 每个 pattern 多做 2-3 道 Medium，确保理解透彻
- 每个 pattern 至少挑战 1 道 Hard
- 加入高级数据结构和并查集
- 每周回顾之前 pattern 的题目（间隔重复）

### 竞赛入门路线

按以下顺序：
1. 数组与哈希 + 双指针 + 位运算（基础）
2. 二分查找 + 栈 + 树（数据结构）
3. 图（BFS/DFS/最短路/拓扑排序/并查集）
4. 动态规划（一维 → 多维 → 区间DP）
5. 高级数据结构（线段树/树状数组）
6. 贪心 + 数学

---

> 此题库由林知栈人格技能维护，作为其教学资源的核心组件。
> 题目来源融合 NeetCode、Sean Prashad LeetCode Patterns、AlgoMonster、代码随想录、labuladong、AcWing 等知识体系。
> 版本：v1.0 | 更新日期：2026-06-03
