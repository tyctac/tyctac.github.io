---
layout: post
title: 机器学习常识
category: 
- ML
tags:
- records ---

#### bias & viaration
1. Bagging 降低方差，不剪枝决策树，神经网络（等易受到样本扰动的学习器上）效果明显
2. 置信度深入解读
#### 过拟合
3. 过拟合 会在哪些情况下出现，（Stacking算法中，直接使用初级学习器的训练集产生次级训练集,为什么，感觉不会啊？）
#### 噪声消除
- overfitting太普遍，对应与不同模型怎么解决，我觉得很多情况下都是因为一些异常点导致的，如果开始消除噪声做的好，overfitting应该能够得到一定的改善吧，但是这应该是治标不治本的方式，但是是通用的缓解的方式，有什么理论解释吗，具体问题还是得通过具体模型的特定的方式去调节吧！！！

#### 规范化措施
1. k近邻算法，对数值大的属性有偏好，调整的方式为归一化，  
2. ID3决策树，对可取值数目较多的属性有所偏好，-->使用增益率来选择最优划分属性
总结，  

#### 朴素贝叶斯
- 对于成人网站分类，如果用加上一的方法实现拉普辣死平滑，会造成多大的误差？？又或者有什么替代的方式呢，已经试过用0.01等方式了，或者这样也是无伤大雅的呢？？凭经验分析的话，另一番情景,采用其他方式的话，————需要规范化？(毕竟概率本身算作是一种特殊的规范化【归一化？】)

#### k决策树，如何改善k近邻的性能
pass
#### 一个机器学习算法的通常的流程：(使用决策树作为例子）
1. 输入：训练集 D = {(x1,y1),...(xm,ym)}  
    	 属性集 A = {a1,a2,...,ad}

#### 特征权重计算
- 有哪些方法???  

#### 问题  
- learning to rank
- 加法模型???
- 指数函数泰勒展开,怎么证明??
- 什么情况该用线性模型?????????
- 经验风险???
