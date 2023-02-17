# 任务书的初步理解

## 标题的思考

### 划分层面

- 深度学习语义分割: Deep Learning based Semantic Segmentation
- 线缆弯曲半径测量: Cable bending radius measurement

---

说明两个角度

- Deep Learning

  - Semantic Segmentation

- measurement

  - bending radius

    Object: Cable

### 深入理解其中的含义

The cable bending radius is a measurement of the smallest radius a cable can be bent around without damaging the cable. Factors which influence the minimum bending radius include the cable size, the cable construction, the conductor type and the sheathing and insulation types used[1].

弯曲半径控制对线缆的使用寿命有重要影响

> 了解到影响因素, 然后影响因素的关系由 deep learning 来学习.
>
> 首先知道准确的定义, 用来做反馈测验

---

- the cable insulated material

  简化模型, 可以认为是固定的某个

  一般生产的时候, 会批量生产某一种, 此时可以输入系数, 认定为材料固定

- the cable construction

- the cable size

- the cable's overall diameter

  需要考虑修正系数

---

1. [How is the minimum bending radius determined for cables?](https://www.elandcables.com/the-cable-lab/faqs/faq-how-is-the-minimum-bending-radius-determined-for-cables)

2. [Cable Bending Radius Calculation](https://blog.keystone-cable.com/cable-bending-radius-calculation)

## 应用的难点

针对全手动线缆弯曲半径检测过程中效率低，精度差，满足高效生产的需求等问题:

- 精度
- 效率

## 使用的方法

应用深度学习语义分割算法实现对线缆特征识别与掩膜分割

- 线缆特征识别
- 掩膜分割

---

在掩膜分割的基础上实现平面线缆的弯曲半径测量

- 掩膜分割的基础上
- 平面线缆

## 评价标准

根据相关标准对线缆弯曲半径做出评价

- 根据相关标准

## 整体理解

- 对象: 平面线缆

  如何描述这个对象

  > 从数学上如何建模, 从代码上用什么的数据结构描述

- 方法:

  - 在掩膜分割的基础上

    ?: 什么是在这基础上

  - 使用深度学习的语义分割

- 目的:(评价的层面)
  - 高精度
  - 高效率
- 评价:(评价的依据)

  - 根据国家标准(侧重于精度)

  查阅其他得到的因素:

  - the cable insulated material

    简化模型, 可以认为是固定的某个

    一般生产的时候, 会批量生产某一种, 此时可以输入系数, 认定为材料固定

  - the cable construction

  - the cable size

  - the cable's overall diameter

    需要考虑修正系数

## 英文描述

Projects to be completed: cables play an important role in power transmission, signal transmission and other fields, and the bending radius control during cable laying has an important impact on the service life of cables. The project aims at the problems of low efficiency and poor precision in the process of fully manual cable bending radius detection, and meets the needs of efficient production. The deep learning semantic segmentation algorithm is applied to realize the cable feature recognition and mask segmentation, which is realized on the basis of mask segmentation. Measure the bending radius of planar cables, and evaluate the cable bending radius according to relevant standards.

?> translated by [Google Translate](https://translate.google.com/)

### 关键术语

- 语义分割: Semantic Segmentation
- 线缆: Cable
- 弯曲半径: bending radius
- 掩膜分割: mask segmentation
- 特征提取: feature recognition

掩膜分割: 应该是一种图像分割

## 反思

!> 误区: 应该自动化提取特征, 而不是我来建模设置特征. 这是深度学习的特点

可以和助教探讨一下, 自己设置特征会怎么样, 可不可以放入到对比里面
