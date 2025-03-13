# CF1866H Happy Sets

## 题目描述

Define a set $ A $ as a child of set $ B $ if and only if for each element of value $ x $ that is in $ A $ , there exists an element of value $ x+1 $ that is in $ B $ .

Given integers $ N $ and $ K $ . In order to make Chaneka happy, you must find the number of different arrays containing $ N $ sets $ [S_1, S_2, S_3, \ldots, S_N] $ such that: - Each set can only contain zero or more different integers from $ 1 $ to $ K $ . - There exists a way to rearrange the order of the array of sets into $ [S'_1, S'_2, S'_3, \ldots, S'_N] $ such that $ S'_i $ is a child of $ S'_{i+1} $ for each $ 1\leq i\leq N-1 $ .

Print the answer modulo $ 998\,244\,353 $ .

Two sets are considered different if and only if there is at least one value that only occurs in one of the two sets.

Two arrays of sets are considered different if and only if there is at least one index $ i $ such that the sets at index $ i $ in the two arrays are different.

## 输入格式

The only line contains two integers $ N $ and $ K $ ( $ 1 \leq N,K \leq 2\cdot10^5 $ ) — the number of sets in the array and the maximum limit for the values in the sets.

## 输出格式

An integer representing the number of different arrays of sets that satisfy the problem condition, modulo $ 998\,244\,353 $ .

## 输入输出样例 #1

### 输入 #1

```
2 2
```

### 输出 #1

```
11
```

## 输入输出样例 #2

### 输入 #2

```
1 3
```

### 输出 #2

```
8
```

## 输入输出样例 #3

### 输入 #3

```
3 1
```

### 输出 #3

```
4
```

## 说明/提示

In the first example, there are $ 11 $ different arrays of sets possible, which are:

- $ [\{\}, \{\}] $
- $ [\{\}, \{1\}] $
- $ [\{\}, \{1, 2\}] $
- $ [\{\}, \{2\}] $
- $ [\{1\}, \{\}] $
- $ [\{1\}, \{1, 2\}] $
- $ [\{1\}, \{2\}] $
- $ [\{1, 2\}, \{\}] $
- $ [\{1, 2\}, \{1\}] $
- $ [\{2\}, \{\}] $
- $ [\{2\}, \{1\}] $

给一个长度为 n，且每个元素大于 1 的数组 $f$，现在有 $q$ 个询问，每次询问给两个整数 $l,r$，
对每个 $l <= i <= r$，求出 $max \{ min(f_i, r-i+1) \} $ 是多少? 
$n <= 1e6$
$q <= 1e6$