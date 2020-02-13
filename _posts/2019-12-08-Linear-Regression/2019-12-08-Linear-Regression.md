---
Title: Linear Regression
edit: 2019-12-08
categories: Machine-Learning 
tags: Linear-regression Least-square-estimation MLE MAP
status: Writing
description: 从最小二乘法及其几何意义讲起来，验证最小二乘法与高斯噪声的MLE以及高斯噪声高斯先验估计下的MAP等价，并在此角度下叙述正则化的作用。
---

$$
\newcommand{\ket}[1]{\vert {#1} \rangle}
\newcommand{\bra}[1]{\langle {#1} \vert}
\newcommand{\braket}[2]{\left\langle {#1}\! \mid \!{#2} \right\rangle}
\newcommand{\Partial}[2]{\frac{\partial {#1}}{\partial{#2}}}
\newcommand{\emath}{\mathrm e}
\newcommand{\ceil}[1]{\left\lceil{#1}\right\rceil}
$$

In previous notes I draw a few triangulations of torus, Klein bottle and cylinder (which is topologically equivalent to a sphere), etc. The problem is to find a minimal triangulation (minimal vertices, triangles or edges). In this post, I am particular interested in minimal triangulation of $2$ dimensional manifolds, especially torus, $2$-torus, ...

在看了很多东西之后，感觉很有必要总结一下用以备忘，并且感觉很多theory都可以串联起来，所以想要开始写Blog了。打算分几条线来写，一部分总结提炼一下最近看过的东西，一部分记录一些思考与想法，还有一部分慢慢把脑子里学过的东西倒出来。

那么这就是把脑子里的东西倒出来系列的第一篇Blog啦！想要从Machine Learning中的线性回归(Linear Regression)开始讲起。

# 最小二乘估计(LSE)



# MLE角度

# MAP角度



# 正则化



# 参考文献



