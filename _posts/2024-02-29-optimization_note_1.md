---
title: 'Optimization Notes No. 1'
date: 2024-02-29
permalink: /posts/2024/08/optimization_1/
tags:
  - Optimization
  - Convex Optimization
---

## 矩阵范数
### 向量范数的推广

$$||A||_1=\sum_{i,j}|A_{ij}|$$

$$||A||_F=\sqrt{\sum_{i,j}A_{ij}^2}=\sqrt{tr(AA^T)}$$

### 算子范数
向量范数诱导

$$||A||_1=\max_{1\leq j\leq n} \sum_{i=1}^m|a_{ij}|$$

$$||A||_2=\sqrt{\lambda_{max}(A^TA)}$$

$$||A||_{\infty}=\max_{1\leq i\leq m} \sum_{j=1}^n|a_{ij}|$$

### 核范数

$$||A||_{*}=\sum_{i=1}^r\sigma_i$$

\\(\sigma_i\\)为\\(A\\)的所有非零奇异值，\\( r=\text{rank} (A)\\).

## 凸集、凸组合、凸包

**凸包**：集合\\(\mathcal{S}\\)的所有点的凸组合构成的集合叫做 \\(\mathcal{S}\\)的**凸包**，记为\\(\text{conv}\mathcal{S}\\).

**凸包的等价定义**：

$$\text{conv} \mathcal{S} = \bigcap_{C\supseteq S, C\text{ is convex}}C$$

即\\(\text{conv}\mathcal{S}\\)为包含\\(\mathcal{S}\\)的最小凸集.




------