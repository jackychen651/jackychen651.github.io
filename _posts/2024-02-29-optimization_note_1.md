---
title: 'Optimization Notes -- Convex Set'
date: 2024-02-29
permalink: /posts/2024/08/optimization_1/
tags:
  - Optimization
  - Convex Optimization
---

# 基础
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

任意多个凸集的交为凸集.

**凸包**：集合\\(\mathcal{S}\\)的所有点的凸组合构成的集合叫做 \\(\mathcal{S}\\)的**凸包**，记为\\(\text{conv}\mathcal{S}\\).

**凸包的等价定义**：

$$\text{conv} \mathcal{S} = \bigcap_{C\supseteq S, C\text{ is convex}}C$$

即\\(\text{conv}\mathcal{S}\\)为包含\\(\mathcal{S}\\)的最小凸集.

## 仿射组合、仿射包

**仿射组合**：去掉凸组合中系数\\(\geq 0\\)的限制，但保留系数之和为1的条件.

**仿射包**：\\(\mathcal{S}\\)所有点的仿射组合构成的集合，记为\\(\text{affine}\mathcal{S}\\).

## 锥组合、凸锥

**锥组合**：去掉凸组合中系数和为1的限制，但保留系数\\( > 0\\)的条件.

**凸锥**：若集合\\(\mathcal{S}\\)中任意点的锥组合都在\\(\mathcal{S}\\)中，则称\\(\mathcal{S}\\)为凸锥.

# 凸集的例子
## 超平面、半空间、多面体、（半）正定锥

**超平面**：形如\\( \{x\vert a^Tx=b, a\neq \textbf{0}\} \\)的集合.

**半空间**：形如\\( \{x\vert a^Tx\leq b, a\neq \textbf{0}\} \\)的集合.

**多面体**：形如\\( \{x\vert Ax\leq b, Cx=d,A\in \mathbb{R}^{m\times n} , C\in \mathbb{R}^{p\times n}\}\\)的集合.

**（半）正定锥**

\\(\mathcal{S}^n\\)：\\( n\times n\\)对称矩阵

\\(\mathcal{S}_+^n\\)：\\( n\times n\\)半正定矩阵

\\(\mathcal{S}_{++}^n\\)：\\( n\times n\\)正定矩阵

# 分离超平面定理


------