---
layout: post
read_time: true
show_date: true
title: "ml之 kernel function "
date: 2021-11-9
img: posts/machinel.jpg
tags: [machine learning]
category: ml
author: HU YANG
description: "my babe"
---
### Kernel Function

#### Objection

解决原始空间数据不可分的问题，想法是**转移到高维可分空间**



#### Definition

把数据从低维（原始空间）映射到高维空间（**特征空间**），并利用某个函数计算**点积**作为**相似性度量**，该函数就是 kernel function。

:chestnut:一个带有特征映射的二维输入空间$\chi\subseteq\mathbb R^2$

特征映射二维到三维 

$\Phi:x=(x_1,x_2)\rightarrow \Phi(x)=(x_1^2,x_2^2,\sqrt{2}x_1x_2)\in F=\mathbb R^3$

特征空间中的内积  

![image-20211109112120045](/home/huyang/huyanghalo.github.io/assets/img/posts/20211109/p2.jpg)
$$
\begin{equation}\begin{split}
<&\Phi(x),\Phi(z)>\\
&=<(x_1^2,x_2^2,\sqrt{2}x_1x_2),(z_1^2,z_2^2,\sqrt{2}z_1z_2)>\\
&=x_1^2z_1^2+x_2^2z_2^2+2z_1z_2x_1x_2
\end{split}\end{equation}
$$


:chestnut: SVM中将低维数据映射到高维空间

![map](E:\huyanghalo.github.io\_posts\assets\img\posts\20211109\svm.jpg)





#### Properity

![map](E:\huyanghalo.github.io\_posts\assets\img\posts\20211109\p1.jpg)



### Commonly used function

##### 1. linear kernel function

$\Phi(x)=x$

也就是说

$\Phi(x,z)=x^Tz$

**特征**：输入空间和输出空间维度一样，适用于原始数据已经是高维的，且线性可分。

##### 2. radial basis function

$\Phi(x,z)=exp(-\frac{||x-z||^2}{2\sigma ^2})$​

$\Phi(x,z)=\Phi(||x-z||)$都叫做  radial basis function,只是使用距离的表示方法不一样。



### Reference

https://blog.csdn.net/mengjizhiyou/article/details/103437423

https://blog.csdn.net/sunflower_sara/article/details/81228112

