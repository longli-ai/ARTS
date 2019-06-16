# Week11 06/09/2019


## Algorithm

### 题目

[908. Smallest Range I](https://leetcode.com/problems/smallest-range-i/)

```
Given an array A of integers, for each integer A[i] we may choose any x with -K <= x <= K, and add x to A[i].

After this process, we have some array B.

Return the smallest possible difference between the maximum value of B and the minimum value of B.

Example 1:

Input: A = [1], K = 0
Output: 0
Explanation: B = [1]
Example 2:

Input: A = [0,10], K = 2
Output: 6
Explanation: B = [2,8]
Example 3:

Input: A = [1,3,6], K = 3
Output: 0
Explanation: B = [3,3,3] or B = [4,4,4]
```

### 要求
- 题目比较难看懂，其实就是从数组`A`中取值，从`[-K,K]`取值，和`A`元素相加，得到一个新的数组`B`。
- 求最后`B`元素中最大值和最小值的最小差值。

### 思路
- 从观察例子可以看出，主要讲数组`A`中最大最小值拿出来
- 让最大值变小，最小值变大，这样能得到最小差值。
- 当然要判断最大值减去最小值的差值是否是`2*K`


### 解答
- [908. Smallest Range I](https://github.com/rubust-ai/Leetcode-python3/blob/master/908_Smallest_Range_I.py)

&nbsp;

## Tips





&nbsp;
## Share

[Be a Better Negotiator in Everyday Life](https://medium.com/s/story/be-a-better-negotiator-in-everyday-life-f7d16afd9ed2)

本文是讨论日常生活中，如何成为一个更好的谈判者

### 作者的`Share`

谈判不应该是需要大量准备的东西，每个人平时都在进行大大小小的谈判。

围绕谈判如此焦虑的一个原因是：人们倾向于将其定义为一个人获胜而另一个人失败的交易。

它甚至可以加强您的人际关系，帮助您学习与您所爱的人更有效地沟通。

以下是如何重新构思您的思维方式，以便更好地在日常生活中询问您想要的内容。

#### 谈判是有一个共同的目标

谈判有两个角度
- 人们常常认为谈判的目的是提出明确的论据，施加压力，或强力支持另一方屈服。
- 但是当你意识到双方都需要同意达成协议时，那么你可以看到，为了更快地达成交易，你需要了解对方想要什么。

**选择共同达成协议**
- 参与者对于在问题中获得理想的结果更加乐观 - 解决方案，更有可能再次合作


##### 调整细节

谈判并不想伤害感情等

谈判中技巧
- 解决冲突最重要的技能是学习倾听和理解
    - 不仅仅是尊重对方，了解对方的需求，而且还给自己保留了时间进行回应和调整。
- 避免使用所谓的“红旗”字样
    - 比如“应该”，“但是”，“永远”和“从不”
    - 改成“推荐”，“建议”和“将要或不会”
    - 控制情绪，减少刺激，并且很直接

- 肢体语言
    - 不坐在一个人的对面
    - 坐在旁边




##### 放下电话

面对面交流更能培养人的感情，并且促使大家共享解决方案。


##### 尽量放松

当你与亲近的人谈判时，很容易感觉真的有两次谈判
- 一个是你实际谈论的
- 另一个是关系本身

深呼吸放松
- 尽量了解对方需求和想法，并且让对方知道你是尊重他的
- 把谈判看成问答环节


### 我的`Share`

在平时生活中，我不愿意谈判或者害怕谈判，比如加薪，买卖房屋，总是将这些看成一件很严肃的事情，内心基本是排斥的。

之前的处理，基本上我都是让对方说，尽可能的说，然后问我，让我回答。

但这样的做法，会让对方或者我自己感受到，我只是被动的在接受某些东西，并没有主动的说出自己的想法，这在工作中是很不利的，影响自身的`promotion`。

有些谈判是一次性的合作，当然可以采用使对方屈服，但是有时候的太强硬会使对方选择其他方案，所以在自己可接受的范围内，`soft`的合作解决问题会更好，但是如果对方大砍刀下来，基本上还是很 `hard`的。


&nbsp;
## Lecture

### 课程 `link`

[Week2 Neural Networks Basics](https://www.coursera.org/learn/neural-networks-deep-learning/home/week/2)

### 笔记 `link`

[Week2 Neural Networks Basics](https://github.com/rubust-ai/Deep-Learning/blob/master/class1-week2.md)

### 作业 `link` - `private repo`

[Week2 Neural Networks Basics](https://github.com/rubust-ai/Deep-Learning-Homework/tree/master/class1/week2)
- [Logistic Regression as a Neural Network](https://github.com/rubust-ai/Deep-Learning-Homework/blob/master/class1/week2/homework/Logistic%20Regression%20as%20a%20Neural%20Network/Logistic%20Regression%20with%20a%20Neural%20Network%20mindset%20v5.ipynb)
- [Python Basics with Numpy](https://github.com/rubust-ai/Deep-Learning-Homework/blob/master/class1/week2/homework/Python%20Basics%20with%20Numpy/Python%20Basics%20With%20Numpy%20v3.ipynb)


