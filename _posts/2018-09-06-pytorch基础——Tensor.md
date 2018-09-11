--- 
layout: post # 使用的布局（不需要改） 
title: PyTorch基础 # 标题 
subtitle: Tensor #副标题 
date: 2018-09-06 # 时间 
author: Yuuu # 作者 
header-img: img/PyTorch基础.jpg #这篇文章标题背景图片 
catalog: true # 是否归档 
tags: #标签 
   - PyTorch 
---

***

```
import torch as t 
import numpy
```

## 构建矩阵
```
   x = t.Tensor(5,3) #构建5*3矩阵
   x = t.rand(5,3) #使用[0,1]均匀分布随机初始化二维数组
```
 
## 查看维度
```
   print(x.size()) 
   print(x.size()[0]) # 第一维的维度
   print(x.size(0)) # 等价于上一行
```
## 运算
```
   y = t.rand(5,3)
   x + y #1

   t.add(x,y) #2
  
   y.add(x) #3
  
   result = t.Tensor(5,3) #4
   t.add(x,y,out=result)
```
 以上四种加法均返回一个新的矩阵，不改变相加的两个矩阵
 inplace运算改变运算矩阵，比如
```
   y.add_(x) 
```
表示将x加到y上，改变了y的值
> 注意：函数名后面带下划线_的函数会修改Tensor本身

##  Tensor 和 Numpy 相互转换
 ```
   b = a.numpy() #Tensor->Numpy
   b = t.from_numpy(a) # Numpy->Tensor
 ```


