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

[6 Science-Backed Strategies to Avoid Choking Under Pressure](https://medium.com/s/story/6-science-backed-strategies-to-avoid-choking-under-pressure-4db788062371)

本文是处理压力相关的，对我们这些做开发的有很大帮助。

### 作者的`Share`

我只看到5种方法

`Don’t think too hard.`

其实就是有些类似`just do it`口号，不想太多，初级着重在技巧和熟练程度上。熟练以后，基本就是身体的本能反应。



`Practice under pressure.`

预防性措施，平时都在安逸的情况下进行学习和排练，真正考试或者演出的时候，基本都是高皮质醇和肾上腺素的情况。要在模拟环境下进行学习和排练。


`Pretend like you’ve already won.`

这种事当你已经处于压力情况下，如何处理。清晰分析自己可以获得什么，失去什么。

`Tell yourself that you’re in control.`

改变自己的观点，来减少焦虑感。

`Give yourself a pep talk.`

改变与自己交谈的方式也可以改变你的表现。


### 我的`Share`

在生活学习工作中，还是有很多次压力山大的时候，感到自己将要窒息，比如高考结束看分数的时候，工作面试前，给高level的老板汇报工作的时候，和老外聊天担心英语，理财亏损巨大的时候。

很多时候，我采用的策略是 `fuck u`，在之前我会认真准备，在压力巨大的时候，我为了冷静自己，就会采用这种策略，就是我接受我现在的表现，我也接受如果出现的失败。在那个时候，面试官，老板你们在我眼里都是`shit`，根本不关心你们当前是怎么评价我的🤦‍♂️。

这种方法有点想破罐子破摔，不过感觉还是不错的。

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


