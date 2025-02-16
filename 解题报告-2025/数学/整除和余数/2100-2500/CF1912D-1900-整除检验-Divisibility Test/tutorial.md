### CF1912D

##### 题意
在 $b$ 进制下，判断某一个数字 $x$ 关于模 $n$ 的同余，具体分 $3$ 种：
从最后一位开始数：
第一种：最后 $k$ 位和 $x$ 模 $n$ 同余。
第二种：$k$ 位一组 相加求和和 $x$ 模 $n$ 同余。
第三种：$k$ 位一组 相加减交替求和和 $x$ 模 $n$ 同余。

##### 解题思路

对于一长串数字 $x = a_na_{n-1}\dots a_2a_1a_0$，它的 $b$ 进制表示为：
$x = a_0b^0+a_1b^1+a_2b^2+\dots+a_nb^n$。
若 $b^k \equiv 0 \pmod{n}$，则 $x$ 和 $a_0b^0+a_1b^1+\dots+a_{k-1}b^{k-1} = a_{k-1}\dots a_1a_0$同余，
对应第一种情况。

若 $b^k \equiv 1 \pmod{n}$，则 $x$ 和 $a_0b^0+a_1b^1+\dots+a_{k-1}b^{k-1}+a_kb^0+a_{k+1}b^1+\dots+a_{2k-1}b^{k-1} + \dots  = a_{k-1}\dots a_1a_0+a_{2k-1}\dots a_{k+1}a_k+\dots$ 同余，
对应第二种情况。

若 $b^k \equiv -1 \pmod{n}$，则 $x$ 和 $a_0b^0+a_1b^1+\dots+a_{k-1}b^{k-1}-a_kb^0-a_{k+1}b^1-\dots-a_{2k-1}b^{k-1}+\dots  = a_{k-1}\dots a_1a_0-a_{2k-1}\dots a_{k+1}a_k+\dots$ 同余，
对应第三种情况。