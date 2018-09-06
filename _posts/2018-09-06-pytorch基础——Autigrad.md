--- 
layout: post # 使用的布局（不需要改） 
title: PyTorch基础 # 标题 
subtitle: Autograd: 自动微分 #副标题 
date: 2018-09-06 # 时间 
author: Yuuu # 作者 
header-img: img/PyTorch基础.jpg #这篇文章标题背景图片 
catalog: true # 是否归档 
tags: #标签 
   - PyTorch 
---

***
##  Autograd
在Tensor上的所有操作, Autograd 都能为它们自动微分， 避免手动计算导数的复杂过程。
autograd.Variable是Autograd中的核心类，它简单封装了Tensor。可以调用.backword实现反向传播，自动计算所有梯度。
代码如下：
```
from torch.autograd import Variable
```
```
#使用Tensor新建一个Variable
x = Variable(t.ones(2,2), requires_grad = True)
```
# 待修改
