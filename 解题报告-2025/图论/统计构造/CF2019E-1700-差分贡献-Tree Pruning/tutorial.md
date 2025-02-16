## 解题思路
考虑贡献法，对于某一个节点 $u$ 它的深度是 $dep$，
它的叶子节点最大深度是 $dep_{ma}$，那么它对最终状态所有叶子
节点深度是 $[0,dep-1]$ 和 $[dep_{ma}+1,\infty]$ 有删掉的贡献。
差分所有贡献即可。


## 题面翻译

给你一颗有 $n$ 个点的以 $1$ 为根的树。

叶子结点定义为**没有子节点**的点。

每一次操作，你可以删掉一个**叶子**结点。

很容易发现这样还会出现新的叶子。

如果要得到一颗所有叶子到根节点距离都相等的树，至少需要操作几次呢？

**输入**

每个测试包含多个测试用例。第一行包含测试用例的数量 $t$ ( $1 \le t \le 10^4$ )。测试用例说明如下。

每个测试用例的第一行都包含一个整数 $n$ ( $3 \leq n \leq 5 \cdot 10^5$ ) - 节点数。

接下来的每行 $n-1$ 包含两个整数 $u$ , $v$ ( $1 \leq u, v \leq n$ , $u \neq v$ )，描述了连接 $u$ 和 $v$ 的一条边。可以保证给定的边构成一棵树。

保证所有测试用例中 $n$ 的总和不超过 $5 \cdot 10^5$ 。

translate by Hoks

## 题目描述

[t+pazolite, ginkiha, Hommarju - Paved Garden](https://soundcloud.com/fractalex-gd/ginkiha-paved-garden-little)

⠀



You are given a tree with $ n $ nodes, rooted at node $ 1 $ . In this problem, a leaf is a non-root node with degree $ 1 $ .

In one operation, you can remove a leaf and the edge adjacent to it (possibly, new leaves appear). What is the minimum number of operations that you have to perform to get a tree, also rooted at node $ 1 $ , where all the leaves are at the same distance from the root?

## 输入格式

Each test contains multiple test cases. The first line contains the number of test cases $ t $ ( $ 1 \le t \le 10^4 $ ). The description of the test cases follows.

The first line of each test case contains a single integer $ n $ ( $ 3 \leq n \leq 5 \cdot 10^5 $ ) — the number of nodes.

Each of the next $ n-1 $ lines contains two integers $ u $ , $ v $ ( $ 1 \leq u, v \leq n $ , $ u \neq v $ ), describing an edge that connects $ u $ and $ v $ . It is guaranteed that the given edges form a tree.

It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 5 \cdot 10^5 $ .

## 输出格式

For each test case, output a single integer: the minimum number of operations needed to achieve your goal.

## 样例 #1

### 样例输入 #1

```
3
7
1 2
1 3
2 4
2 5
4 6
4 7
7
1 2
1 3
1 4
2 5
3 6
5 7
15
12 9
1 6
6 14
9 11
8 7
3 5
13 5
6 10
13 15
13 6
14 12
7 2
8 1
1 4
```

### 样例输出 #1

```
2
2
5
```

## 提示

In the first two examples, the tree is as follows:

 ![](https://cdn.luogu.com.cn/upload/vjudge_pic/CF2018C/46789adad3b93ca642b297f7ca0ca574c7f98f60.png)In the first example, by removing edges $ (1, 3) $ and $ (2, 5) $ , the resulting tree has all leaves (nodes $ 6 $ and $ 7 $ ) at the same distance from the root (node $ 1 $ ), which is $ 3 $ . The answer is $ 2 $ , as it is the minimum number of edges that need to be removed to achieve the goal.

In the second example, removing edges $ (1, 4) $ and $ (5, 7) $ results in a tree where all leaves (nodes $ 4 $ and $ 5 $ ) are at the same distance from the root (node $ 1 $ ), which is $ 2 $ .