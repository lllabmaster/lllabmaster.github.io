---
layout: post
title: tfrecord知识点
date: 2019-10-12 15:32:24.000000000 +09:00
---


## tfrecord

 
**tfrecord文件中，主要涉及的几种概念**：

 层次 | 类 
 --- | --- 
 存储数据类型 | tf.train.BytesList，tf.train.FloatList，tf.train.Int64List
 存储特征结构 | tf.train.Feature，tf.train.FeatureList
 存储样本结构 | tf.Example，tf.SequenceExample

1. 首先tfrecord文件中，每一条数据，是一个tf.Example或者tf.SequenceExample，这表示一条样本
2. 在样本中，存在很多维特征，其中每一维特征，都可以表示为tf.train.Feature或者tf.train.FeatureList
3. 那么在一维特征里，具体存储的数据值，就是tf.train.BytesList，tf.train.FloatList，tf.train.Int64List之一（只能在这三种之中）