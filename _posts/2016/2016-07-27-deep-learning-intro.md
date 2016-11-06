---
layout: post
title: 深度学习起步
categories:
- Deep Learning
tags:
- DL
- AI
---

深度学习作为机器学习的一个分支也发展了也很多年了，只是一直感觉特别遥远，高深莫测，所以一般都不会接触到。不过近些年深度学习被越来越多的提起，特别是年初AlphaGo和李世石的比赛，打破了电脑在围棋上无法击败人类的预言，深度学习再次被推上风口浪尖。这两年逐渐火起来的自动驾驶，背后也是深度学习，像Google的自动驾驶汽车都需要不断地行驶在真实的路面上进行“学习”。最近流行的Prisma照片艺术化处理软件，其背后的技术也是深度学习：[A Neural Algorithm of Artistic Style](http://arxiv.org/abs/1508.06576)。

我们先从机器学习开始吧，通俗点讲机器学习就是指计算机程序随着经验积累而自动提高性能。在机器学习界有一个类似于编程语言中的Hello World问题，即手写数字识别问题，一般都是通过[MNIST](http://yann.lecun.com/exdb/mnist/)（Mixed National Institute of Standards and Technology）手写数字图片数据库来训练程序，最后再通过对应的测试数据来测试，得出识别率。
也就是说如果一个程序对手写数字图片识别的准确率随着不断的训练识别率不断得到提升，那么可以称计算机程序在从训练中进行学习。这里有几个概念，首先任务，这里就是对输入的某个手写图片进行识别；然后是训练，训练则是训练数据，上面的书写数字识别的训练数据便是大量的手写数字图片以及对应的答案；还有就是识别率，识别率会随着不断的学习而变得越来越高，也就是通过学习，程序自己改了自己内部的一些状态，使得对新的手写图片进行识别的时候更加准确。

再来抽象点进行描述，机器学习就是类比人类认识世界的过程，人类通过历史经验进行归纳总结，碰到新的问题后能够根据归纳总价的规律来解决问题。当然机器没有人类大脑这么牛逼的硬件，而有的只是一堆集成电路和软件程序，对于机器学习来讲，机器学习软件通过训练数据来调整优化软件内部计算模型的参数，然后通过优化后的模型参数来处理新的数据，得到结果。

机器学习可以分为两大类：监督学习和无监督学习。监督学习就是训练数据给出数据以及数据对应的标准答案，学习后，对训练样本外的数据做出分类预测；非监督学习就是对没有答案或者标记的数据进行学习，发现数据的结构特性，将相似的数据聚集在一起，这就是所谓的聚类了，聚类并不关心某一类是什么。

我们再来谈谈机器学习的训练数据库，目前在机器视觉这方面比较好些，除了上面Hello World的MNIST数据库，还有全球最大的图像识别数据库[ImageNet](http://image-net.org/),它的缔造者就是斯坦福大学的李飞飞教授，他们利用互联网图片以及众包技术平台来帮助标记这些图片，所以这些图片数据库的构建可以说是“人肉计算”。斯坦福大学每年都会举行一个比赛，邀请谷歌、微软，百度等 IT 企业使用 ImageNet，测试他们的系统运行情况。每年一度的比赛也牵动着各大巨头公司的心弦，过去几年中，系统的图像识别功能大大提高，出错率仅为约 5％ ，比人眼还低。还有一个数据库就是[MSCOCO](http://mscoco.org/) ,由微软资助，每年也会举行比赛。

再来说说深度学习，所谓深度是相对于浅层结构的机器学习，这些典型结构包含至多一层或两层非线性特征变换。而深度学习则是增加了计算的层次，原始的数据输入后，会经过多层处理之后才会最终输出得到结果。网络很多都提到深度学习是对人类视觉皮层结构的模拟，但是实际上深度学习的结构更多来源于理论、直觉和经验探索，和神经科学的相关性并没有那么大。拿深度学习中的卷积神经网络来说，确实部分灵感来自于神经科学，但是其和人类大脑的差距还是很大，所以在宣传的时候如果着重强调“神经”这个关键词会给人以错觉。

上面谈到了深度学习的 多层结构，其实里面的每一层都是一些数学计算，有些层里面的节点都包含一些典型的算法，通常我们都是从“回归”相关的算法开始说起，后面会对回归算法进行详细讲解。
