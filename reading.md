# 文献阅读

- [机器学习、神经网络、深度学习区别](https://blog.csdn.net/WangYouJin321/article/details/90691112)

  Deep learning is a particular kind of machine learning that achieves great power and flexibility by learning to represent the world as nested hierarchy of concepts, with each concept defined in relation to simpler concepts, and more abstract representations computed in terms of less abstract ones.

  在机器学习方法中，几乎所有的特征都需要通过行业专家在确定，然后手工就特征进行编码

  深度学习算法试图自己从数据中学习特征

我的误区: 深度学习会自己提取特征, 所以我不需要一开始 flat cable 建模特征

---

- [卷积神经网络和深度神经网络的区别是什么？](https://www.zhihu.com/question/29366638)

  - 局部感受野(local receptive fields)
  - 共享权重(shared weights)
  - 池化(pooling)

    > 可以进一步看看'一句话总结'相关的内容

---

何雨岩.基于深度学习的图像语义分割综述[J].长江信息通信,2023,36(01):77-79.

---

- [ ] [神经网络与深度学习](https://nndl.github.io/nndl-book.pdf)

  author: [邱锡鹏](https://xpqiu.github.io/) 复旦计算机院

  an online book

  ?> 不知道能不能找他玩耍:thinking:

---

觉得是用卷积神经网络, 需要了解一下

## issue

当前的页面有个问题: 虽然在学习的过程是一个时间上线性的模型, 但在逻辑上, 有些内容我不能立即阅读完, 而是拓展的内容, 应该是像'队列'一样, 暂时能移入到队列中

单单的一维的纵向结构不能良好地表达思考, 需要有一个横向的结构, 同时二者结构能够交互. 可以试试往 monad 方向想想

总结: 当前布局限制了表达, 反作用于限制了思考

---

时间上也有一个问题: 我有其他的事情会打断当前的思考, 需要一种方式类似于 stack, 可以 push, 冻结当前的事务, 下次有时间再来 pop

我想保证我思考的连续

example:

- 我在看某些文章, 有些概念不懂, 或者看看什么拓展的资料. 为保证阅读文章的连贯, 我应该继续阅读, 而这些衍生的东西, 应该能放到队列当中
- 睡觉, 吃饭, 娱乐都会打断我的思考, 我从哪里回复思考是个问题

已有的方案:

- 当某个问题深深困扰我的时候, 睡觉在梦里都会思考
- 当睡前有某种粗略的解决方案的时候, 一早醒来会立马接着原来的思考继续

!> 问题是这需要我真心地被这个问题缠绕住了, 很难进入这个状态, 一般在数学和编程上面. 在英语问题上面, 完全不行

---

希望将上述的思考进一步抽象, 看到有什么模式存在, 然后能够实现自动化
