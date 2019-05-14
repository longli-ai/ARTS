# Week7 05/12/2019

## GitHub公式显示插件
Github 的 markdown 不支持数学公式, 安装下面的 chrome 安装 mathjax 插件，可以正常看 markdown 文中的数学公式，当然前提是你需要过墙，才能安装。

[Github with mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)

&nbsp;
## Algorithm

**题目**

[167. Two Sum II - Input array is sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)

**题目要求**
- 从一个排列好的列表中，找出两个元素，之和是要寻找的数
- 返回的列表中位置+1，第多少个元素。


**解题思路1**
- 我采用倒序来取元素，因为正序需要切片
- 目标值减去当前值，得到差值，如果差值也在列表中，就可以返回了
- 此思路时间效率太差，大概`2192 ms`

**解题思路2**
- 活用二分查找法
- 本题相当于查找两个数字，而不是以前的一个
- 将首尾初始化作为两个元素，看看是否大于target
    - 等于直接返回
    - 大于的话，右边值需要向左移动
    - 小于的话，左边值需要向右移动
- 时间只有 `44 ms`

**我的解法**
[167_Two_Sum_II_Input_array_is_sorted.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/167_Two_Sum_II_Input_array_is_sorted.py)

&nbsp;
## Tips

[docker 入门](https://yeasy.gitbooks.io/docker_practice/content/image/pull.html)

不错的入门书

```bash
docker pull ubuntu:18.04 # 获取镜像
docker run -it --rm \
    ubuntu:18.04 \
    bash

 docker image ls # 列出镜像   
 docker image rm [选项] <镜像1> [<镜像2> ...] # 删除镜像
```

&nbsp;
## Share

[The Bullish Case for Bitcoin](https://medium.com/@vijayboyapati/the-bullish-case-for-bitcoin-6ecc8bdecc1)

- 写的不错，2018年3月，比特币潮水退去的时候写的文章。


[比特币价值的本质是什么?](https://mp.weixin.qq.com/s/7ga-UNTvMWH_TinXipnLpQ)

- 写在2017年12月比特币价格最高峰的时候文章。

作者结论是**价值的本质是共识！**


`从严格意义来说，我们每个月账单所消费的金额，大部分都不是生存的必要，但却是生活的必要。`

心真痛，说的就是我，其实每个月消费的大部分不是你生存必要，生存的衣食住行并没有花费我们很多，而是除这些以外的，比如为了面子方便，选择高品质的住宿和出行，还有穿奢侈品和吃大餐，还有娱乐学习等。所有的附加和不必要的开支，其实是生活的必要。

大部分人还是为了改善生活吧，多了也不敢说，有点超纲。


&nbsp;
## Lecture

[Introduction to TensorFlow](https://www.coursera.org/learn/introduction-tensorflow/)



#### 课程笔记

[Week1 A New Programming Paradigm](https://github.com/rubust-ai/Introduction-to-TensorFlow/blob/master/week1.md)


[Week2 Introduction to Computer Vision](https://github.com/rubust-ai/Introduction-to-TensorFlow/blob/master/week2.md)


[Week3 Enhancing Vision with Convolutional Neural Networks](https://github.com/rubust-ai/Introduction-to-TensorFlow/blob/master/week3.md)


[Week4 Using Real-world Images](https://github.com/rubust-ai/Introduction-to-TensorFlow/blob/master/week4.md)


&nbsp;
## 尾巴

本周有些烦躁，明天会好好努力的，工作赚钱的同时，不忘学习，提升自己。
