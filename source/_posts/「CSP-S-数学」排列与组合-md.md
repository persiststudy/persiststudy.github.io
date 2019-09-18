---
title: 「CSP-S 数学」排列与组合.md
date: 2019-09-18 16:47:20
tags: [CSP-S]
categories: [编程, 数学知识]
---

<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
  
计数原理、排列、组合、递推关系、等差数列求和公式、自然数平方和公式、二项式定理。

## 计数原理
### 加法原理
做一件事有$n$种途径，每种途径有$p_i$个不同的方案，则做这件事的方案数为
$$
\sum_{i=1}^n p_i
$$


乘法原理
做一件事有  个步骤，每个步骤有  个不同的方案，则做这件事的方案数为


容斥原理
统计多个集合的并的元素数量：先加上所有集合的元素的元素数量，再减去『多加的』每两个集合相交的元素数量，再加上『多减的』每三个集合相交的元素数量 ……

即等式左边是多个集合的并的元素数量，等式右边每一项是几个几何的交的元素数量，每一项的符号取决于元素数量的奇偶。

排列
全排列
把  个元素按照不同顺序排列，设总方案数为 （定义 ），考虑第一个元素摆放的位置，得出公式


即 。

普通排列
从  个元素中取  个，按照不同顺序排列，设总方案数为 ，每次选一个数，第一次有  种选择，第二次有  种选择，直到第  次有  种选择，即


将上式与  对比，缺少  及之后的项，即


有重复元素的全排列
从  种元素，第  种有  个，设 ，为了保证答案不重复，可以先求出 ，再除去每种元素重复的情况，即


组合
组合数
从 n 个元素中选择 k 个，顺序无关，设总方案数为 。把排列数  看做先从 n 各种选择 k 个元素，再对 k 个元素做全排列，即


移项得


组合数的性质
 全选或全不选只有一种方案。

 选择  个拿走相当于选择  个留下。

 考虑最后一个选还是不选（Pascal 公式，常用来递推计算组合数表）。

可重复选择的组合
从 n 种无限多的元素中选择 k 个，共有  种方案。

组合数的计算
组合数表
用 Pascal 公式递推，组合数太大要开高精度或者取模。

BigInt combo[MAXN + 1][MAXN + 1];

inline void makeComboTable() {
    for (int i = 1; i <= MAXN; i++) {
        combo[i][0] = combo[i][i] = 1;
        for (int j = 1; j < i; j++){
            combo[i][j] = combo[i - 1][j] + combo[i - 1][j - 1];
        }
    }
}

inline BigInt &C(int n, int k) {
    return combo[n][k];
}
单个计算
书上有用 double 来算的，因为中间乘法 long long 可能会溢出，不知道那样会不会损失精度。

long long C(long long n, long long k) {
    long long result = 1;
    for (int i = 1; i <= k; i++) {
        result = result * (n - i + 1) / i;
    }
    return result;
}
递推关系
Fibonacci 数列
楼梯上共有  个台阶，一次可以走一个或两个，总方案数为


边界为


Catalan 数
给定一个凸  边形，用  条不相交的直线将它剖分成  个三角形，设方案总数为 。

对每个顶点编号，第  个顶点编号为 。作三角形 （），该三角形左边是一个 边形，右边是一个  边形，即


公式
等差数列
设数列  对于任意的  满足 ，则有


求和公式为


自然数平方和

不会证。

二项式定理

