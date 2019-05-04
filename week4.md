# Week4 04/21/2019


### GitHub公式显示插件
github 的 markdown 不支持公式, 安装下面的 chrome 安装插件，可以正常看 markdown 文中的公式，当然前提是你需要过墙。

[github with mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)


## Algorithm

[1021. Remove Outermost Parentheses](https://leetcode.com/problems/remove-outermost-parentheses/)

**题目要求**
- 去掉由'('和')'组成的配对字符串最外面一层括号
- "(()())(())" 得到 "()()()"
- 字符串由'('和')'组成，并且一定会配对

**解题思路**
- 这里面就不用考虑两个问题，第一个出现其他字符串，第二就是一定会配对，不用考虑不配对的情况，题目就是解的一部分。
- 直接循环来查询所有元素
- 一共两种字符串，设立flag来判断，出现'('就+1，出现')'就-1
- 当出现'('时候，先判断flag=0，代表目前是最外面层，是的话不输出
- 当出现')'时候，先判断flag=1，代表目前是最外面层，是的话不输出

**我的解法**

[1021_Remove_Outermost_Parentheses.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/1021_Remove_Outermost_Parentheses.py)

PS：目前这道题是新题目，Leetcode 没有太多解法，所以我的基本上就打败了100%的解法。看到一个解法将flag设置成左右两个count，感觉有点费力，还不如flag。




## Tips

[矩阵求导法则与性质](https://blog.csdn.net/crazy_scott/article/details/80557814)

Octave矩阵求解逻辑回归的损失函数对$\theta$偏导数
$$J(\theta) = \frac{1}{2m}(X\theta-y)^T(X\theta-y) \tag{1}$$

$$\frac{\partial}{\partial\theta}J(\theta) \tag{2}=\frac{1}{m}X^T(X\theta-y)$$




## Share

本周分享的是下面这篇文章，也是方法论相关。

[How to escape tutorial purgatory as a new developer — or at any time in your career.](https://medium.freecodecamp.org/how-to-escape-tutorial-purgatory-as-a-new-developer-or-at-any-time-in-your-career-e3a4b2384a40)

本文核心
- 不要去学完教程再去做项目，而是做项目过程中学习教程。
- 下面这篇是和本文相关的，之前分享过，做事方法论。

[How to think like a programmer — lessons in problem solving](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2)

实现目标方法论
- 明确目标
- 拆分目标
- 实现小目标
- 给予奖励



上面分享第一篇文章中，于我收获最大的，莫过于下面这段话了，与大家共勉。
> Eventually, I came to realize that I needed to stop watching tutorials, abandon my comfort zone, and build a project on my own, without all the instructions neatly laid out for me.

- **学习是舒适区**。学习和娱乐比，娱乐是舒适区，**但是，解决问题和学习比，学习是舒适区**。解决问题比单纯的被灌输知识来说，要难的多。从某种意义上，你只想去学习，其实是你只想呆在自己的舒适区，并想回避去解决问题。认为当自己学会了，问题就会自然而然的解决了。这在工作上是不可行的，主要原因，没时间让你学习。我本身就是仓鼠症(收集资料癖好)，资料一堆，实际问题并没有解决，我就是想通过收集资料，来完成查询资料自己解决问题，这是很可笑的，就是喜欢呆在舒适区。
- **孤立学习效果也不好**。从人脑深层次的原因是大多数学过的指数都不会再去使用，学到的这些零散孤立的知识点不会和其他的知识进行交叉延伸发展，便不会在脑海中长期记住的，这个是我在另外一门公开课 Learn by how to learn 中学到的。所以学东西要讲所有知识点串在一起，比如做项目中，你首先全局知道第一步，第二步，第三步干啥，然后第一步需要完成啥，怎么完成，其他步也一样，你通过这种方式将知识联系在一起。

## Lecture

[Stanford Machine Learning Week5](https://www.coursera.org/learn/machine-learning/home/week/5)

主要内容

神经网络学习
- 代价函数，反向传播算法，反向传播直观展示
- octave中长向量化梯度，梯度检查（验证反向传播正确工作），随机初始化参数，如何实施神经网络
- 无人驾驶
    - 通过路况图片压缩输入，人的左右转动方向盘幅度作为标签y

我的笔记

[week5 notes](https://github.com/rubust-ai/CS229-Machine-Learning/blob/master/week05.md)

&nbsp;
[Stanford Machine Learning Week6](https://www.coursera.org/learn/machine-learning/home/week/6)

主要内容

机器学习建议
- 遇到模型不行，怎么进行debug，节约时间
- 评估假设函数，引入划分数据集两份，计算测试集的error
- 模型如何选择，比如多项式的度，引入了交叉验证，划分数据集成三份
- 过拟合和欠拟合
    - 展示$error-\lambda$
    - 展示$error-m$
- 总结怎么调试模型

机器学习系统设计
- 设计检查垃圾邮件算法
    - 怎样花时间进行提高准确率
- 系统设计tips，即快速实现简单的算法模型，然后手工观察识别出错的数据，说不定进一步提升模型
- 正负样本的数量差距很大的处理
    - 预测稀少样本查准率和查全率的引入
    - tradeoff和f1 score
- 大量数据的有效性

我的笔记

[week6 notes](https://github.com/rubust-ai/CS229-Machine-Learning/blob/master/week06.md)

&nbsp;

## 尾巴
从上周开始啃达叔机器学习第五周，学的比较毛躁，主要原因跟不上反向传播，看了其他人的基本也没大搞明白，有好几次都要放弃了。在星巴克也看不下去了，目前也就是图书馆还能学下去。昨天学完了第6周。今天早晨学完第7周，SVM 也比较难懂，还需要巩固看看自己哪些地方没明白。

达叔又又开课了，这次是 tensorflow 培训，跟不上达书开课的节奏了。除了机器学习之外，还有深度学习，AI for everyone。

本年度的任务就是家里大扫除，减少物品依赖，干掉仓鼠症，尤其是各种书籍，衣服，还有nas里面的电视剧，学习资料，提高生活质量。