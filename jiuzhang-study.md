# 复杂度理论

时间复杂度-核心考察点

空间复杂度-次要考察点

编程复杂度-能看得懂

思维复杂度-能想得出 

## 时间复杂度

* P问题Polynomial多项式

O(N), O(N^2), O(N^3)

O(n + m), O(根号n), O(1)

O(logn), O(nlogn)

* NP问题Nondeterministic Polynomial非多项式解法

O(2^n), O(n^n), O(n!)

时间复杂度考虑最坏情况

### 几个问题

1. 只考虑最高项

O(2^n + N^2) = O(2^n)

O(N^3 + 1000N^2) = O(N^3)

2. 不考虑常数项和系数

O(100N + 1000) = O(1N)

O(logN) = O(log(N^2)) = O(log4(N))

---

O(n+m)和O(max(n,m))哪个大

n + m > max(n, m) > (n + m) / 2

O(n + m) > O(max(n, m)) > O((n + m) / 2)

O(n + m) = O((n + m) / 2)

所以O(n+m) = O(max(n,m))

### 根据时间复杂度倒推算法

一般面试问某个算法的复杂度是什么, 同时也可以倒过来推, 根据时间复杂度倒推算法

O(N)的算法有哪些:

双指针, 打擂台(遍历取最大值), 单调栈, 单调队列

# 双指针算法

相向双指针(判断回文串), 背向双指针(最长回文串, 频率低), 同向双指针

## 相向双指针

* Reverse型
  * 翻转字符串
  * 判断回文串
* Two Sum型
  * 两数之和
  * 三数之和
* Partiton型(分割成两部分, 各自满足要求)
  * 快排
  * 颜色排序

## 例题

### 有效回文串

[valid palindrome](https://www.lintcode.com/problem/415/)

```
描述
给定一个字符串，判断其是否为一个回文串。只考虑字母和数字，并忽略大小写。

样例 1:
输入: "A man, a plan, a canal: Panama"
输出: true
解释: "amanaplanacanalpanama"

样例 2:
输入: "race a car"
输出: false
解释: "raceacar"

样例 3:
输入: "1b , 1"
输出: true
解释: "1b1"

挑战
O(n) 时间复杂度，且不占用额外空间。
```

