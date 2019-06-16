# Week10 06/02/2019


## Algorithm

**题目**

[476. Number Complement](https://leetcode.com/problems/number-complement/)


**要求**
- 求正整数的补数

**思路**
- 根据补数的定义，将数字转换成二进制，按位进行0，1替换，转换成10进制，得到补数

**解答**
- [476. Number Complement](https://github.com/rubust-ai/Leetcode-python3/blob/master/476_Number_Complement.py)

&nbsp;

## Tips

### `numpy`中的广播`broadcasting`

本周做`Lecture`中的`quiz`，`numpy`题目基本都错的，原因是没搞清楚广播。

```python
import numpy as np
arr1 = np.array([[0, 0, 0],[1, 1, 1],[2, 2, 2], [3, 3, 3]])  #arr1.shape = (4,3)
arr2 = np.array([1, 2, 3])    #arr2.shape = (3,)
arr_sum = arr1 + arr2
print(arr_sum)

'''
[[1 2 3]
 [2 3 4]
[3 4 5]
[4 5 6]]
'''
```

我当时认为两个`shape` 大小不一致，应该输出报错，其实是不知道 `numpy`的广播机制。


### 广播的原则

定义
- 如果两个数组的后缘维度（`trailing dimension`，即从末尾开始算起的维度）的轴长度相符，或其中的一方的长度为1，则认为它们是广播兼容的。广播会在缺失和（或）长度为1的维度上进行。

&nbsp;

上例中arr1的shape为（4,3），arr2的shape为（3，)，上面的例子中，`shape`不一致，但是尾巴都是3，是一致的。
![tips1](https://user-images.githubusercontent.com/41643043/59562642-a40c2e80-9061-11e9-8d21-ba44fe2ff191.png)

同样下面的例子也是可以的

![tips2](https://user-images.githubusercontent.com/41643043/59562643-a40c2e80-9061-11e9-8e3c-91508257d771.png)


### 数组维度相同，其中有个轴为1

```python
import numpy as np

arr1 = np.array([[0, 0, 0],[1, 1, 1],[2, 2, 2], [3, 3, 3]])  #arr1.shape = (4,3)
arr2 = np.array([[1],[2],[3],[4]])    #arr2.shape = (4, 1)

arr_sum = arr1 + arr2
print(arr_sum)

'''
[[1 1 1]
 [3 3 3]
 [5 5 5]
 [7 7 7]]
'''
```

但是它们可以执行相加操作，这就是通过广播完成的，在这个例子当中是将arr2沿着0轴进行扩展

![tips3](https://user-images.githubusercontent.com/41643043/59562776-601a2900-9063-11e9-8253-2316e3ca75fb.png)



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

课程 `link`


[Neural Networks and Deep Learning](https://www.coursera.org/learn/neural-networks-deep-learning/home/week/1)

笔记 `link`

[Week1 Introduction to deep learning](https://github.com/rubust-ai/Deep-Learning/blob/master/class1-week1.md)


