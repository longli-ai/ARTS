## Week0 03/24/2019



## Algorithm

### [13. Roman to Integer](https://leetcode.com/problems/roman-to-integer/)

题目要求
- 将罗马数字转换成阿拉伯数字
- 罗马数字比正常数字多的方面，就是有"5/50/..."这种概念
- 还有就是“4/9/40/90/..."这种概念

解题思路
- 第一步是map罗马数字和真实数字
- 第二步是切分s，这个我有些麻烦，主要是没搞清楚s[0:2]和s[2]结果的区别。s[0:2]是第0到第1数字，s[2]第2个数字。耗费了时间在while上
- 第三步就是累加所有值
- 看了看评论区的解答，感觉思路和code基本相同，别人居然56ms，感觉服务器有问题
- Solution[013_Romant_to_Integer.py](https://github.com/longli-ai/Leetcode-python3/blob/master/013_Romant_to_Integer.py)

## Review

### [Logistic Regression — Detailed Overview](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc)

- 逻辑回归，即对数几率回归，处理分类问题，线性回归没有边界，逻辑回归建立在线性回归上，构建出分类模型，严格服从0-1的分布。
- 采用损失函数是log loss，原因线性回归的mse是非凸函数，有局部最低点，所以我们需要一个凸函数，这样才能找到全局最低点，loss才能下降，准确度上升。

## Tips

### [sed命令用法详解](https://www.cnblogs.com/maxincai/p/5146338.html)

- terminal上直接用sed，可以省去用vim打开文件，当然vim的功能比起sed要强悍很多
- sed的正则表达式基本和vim/perl/python基本是相通的
- 可以用在terminal上抓取相关信息用，比如配合grep/ps/ls等等
- 另外可以嵌入perl/python中

## Share

### [How to think like a programmer — lessons in problem solving](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2)


####  实现目标方法论
- 明确目标
    - 明确目标是要做什么，需要完成什么
- 切碎目标
    - 将目标尽可能的切成一个个小的目标
    - 目标必须足够小，并且能实现，否则继续切分小目标
- 实现小目标
    - 检查目标能实现么，不能继续切分目标
    - 利用内部或者外部的方法，实现小目标
- 给予小目标奖励
    - 当完成小目标的时候，要及时给予奖励，比如散步，打游戏，聊天，等等，要根据目标程度给予奖励
    
    
#### PS结尾
- 为什么会点开这篇文章。自从本科毕业发现自己在思考上面有很大问题，做事情大部分时间凭第一感觉去猜。很多时候希望自己能思考以后再得出答案，而不是随口得出一个毫无逻辑的答案和想法。
- 本文大部分内容我已经知道，并且去年已经在践行了。但是也发现自己在解决问题上的误区，有些地方读起来有切身体会。
- 比如**总想完整解决一个问题的方法，不想将问题进行切片**，总想一下子就解决，很多时候，没解决，然后浪费很长时间，有时候直接放下，有时候还要切片去解决问题。
