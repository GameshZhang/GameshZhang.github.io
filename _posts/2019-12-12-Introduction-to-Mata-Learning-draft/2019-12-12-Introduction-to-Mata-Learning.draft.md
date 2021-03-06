---
title: How-to-write-a-draft
categories: categories
tags: tags
keywords: evolution 
description: This is my wild thoughts on the legacy of humanity. This is a diary of a physicist in 4019 A.D.
numbering: false
toc: false
---



前天听组会，李东达师兄的talk介绍了一部分Mata Learning的内容，之前在看Auto-ML的时候也看到过这个概念，talk听下来感觉非常有意思，这个领域有很多我感兴趣的优化上的东西，所以想开个坑，深入了解一下...

# 理想的Mata Learning算法

keyword：快速学习新任务的模型

要能够根据任务去修改自身的基本结构、参数空间，最好能合理的使用训练的先验信息。

# 来自人类行为的两种思路

人类是怎么快速学习新任务的：

1. 人总是能将在之前的任务中学到的信息在新任务上或重复或迁移的使用。
2. 人在生活的过程中，不断学习新的任务会不断建立新的突触连接，建立更高效的神经结构，使得之后面临别的任务时表现更好。

这两个idea相互接近正交，一般可以协同的来考虑。



# 单样本学习(one-shot learning)

如何在某个类别仅有一个样本的情况下，学习对这个类别进行分类。

why hard：从传统ML的思维来说，当只有一个样本(即样本过少的极端情况)，必然会产生过拟合，这在数学上可能会表现为伪逆矩阵不可逆，正规方程不可解。

那么解决这个问题需要做什么？

我们需要让Model在一个样本中学习到 1) 这个类别与别的类别的关键区别在哪 2) 这个类别内的样本的变化范围

其实最本质的问题还是1)

于是在实际中，one-shot learning最常见的方法是Embedding，学习一个嵌入空间，在空间中计算两个不同类别的表示的距离。即要学习到两个不同类别的分布间差异最大的Top-k维特征，并且学习如何将输入数据转化成最相关的维度。

# 总结

一个是根据一些采样点，找到从从起始点到这些采样点的路径及其描述，然后对于其他的点，主要看其相对于已知采样点的距离位置关系，插值估计到达这些点的路径，这其实就是迁移学习，few shot learning的思路。

一个是从采样点来直接寻找从初始点到达任意一点的最优路径的描述（比如从某个初始点到达任意一点的测地线方程的方程形式），这基本就是MAML的理想目标, 也差不多是NAS中Smash的图像。

一个是通过采样点来直接预测地貌，形成对地貌的统一描述，即对地貌的度量的描述，有了这个度量的描述就可以找到到达任意一点的路径；

这三个阶段的难度应该是逐渐增加的，所需要的信息越来越多。

当然，还可以在更高层次上继续玩meta learning of meta learning，即如何学习设计可以完成meta learning的系统

# 参考文献

https://blog.csdn.net/senius/article/details/84483329

https://www.leiphone.com/news/201804/LcJjdu02uSInG5UZ.html