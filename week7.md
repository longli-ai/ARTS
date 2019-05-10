# Week7 05/12/2019

## GitHub公式显示插件
Github 的 markdown 不支持数学公式, 安装下面的 chrome 安装 mathjax 插件，可以正常看 markdown 文中的数学公式，当然前提是你需要过墙，才能安装。

[Github with mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)

&nbsp;
## Algorithm

[191. Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/)

**题目要求**
- 求转成2进制以后，1的个数

**解题思路**
- 比较简单，直接转化成二进制，在转化成list，再数个数。
- 直接用`list(bin(n)).count('1')`就可以了
- 其中需要注意的是'1'已经是string了

**我的解法** 
[191_Number_of_1_Bits.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/191_Number_of_1_Bits.py)

&nbsp;
[461. Hamming Distance](https://leetcode.com/problems/hamming-distance/)

**题目要求**
- 其实就是比较两个数字，按位与，看看不同的有几个，不够的，前面补0

**解题思路**
- 之前没做出来，已经因为list和二进制没搞清楚
- 首先转化成二进制，再转化成list
- 比较两个数字，长度不够，前面加0
- 比较两个数字，1位不同的个数

**我的解法**

[461_Hamming_Distance.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/461_Hamming_Distance.py)


## Tips

`Tensorflow Debug Tips`

在用 `Tensorflow` 炼丹的时候，有时候达到自己想要的精度(loss < 0.4 or acc > 0.98)，怎么停止运行。


```python
class myCallback(tf.keras.callbacks.Callback):
    def on_epoch_end(self, epoch, logs={}):
        if(logs.get('loss') < 0.4):
            print('\nLoss is low so cancelling traning!')
            self.model.stop_training = True

callbacks = myCallback()
(x_train, y_train), (x_test, y_test) = mnist.load_data()
x_train = x_train/255.0
x_test = x_test/255.0

model = tf.keras.models.Sequential([
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(512, activation=tf.nn.relu),
    tf.keras.layers.Dense(10, activation=tf.nn.softmax)
])

model.compile(optimizer='adam',
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

model.fit(x_train, y_train, epochs=10, callbacks=[callbacks])
```





## Share

[Lessons learned from my journey as a self-taught developer](https://medium.freecodecamp.org/lessons-learned-from-my-journey-as-a-self-taught-developer-41b97067730)

### 作者的 `share`

**专注于过程**

很多时候不想学习，不想知道代码的逻辑是啥，然后就是复制和粘贴，为了完成功能(结果导向)。学习任何大的东西，都需要分解成一个个小的步骤，然后掌握每个步骤。

而且每次要学到核心上，将其挂到自己的知识树上，学的时候慢一点，总比回头学要强很多。
```It is better to take many small steps in the right direction than to make a great leap forward only to stumble backward.```

**`Stackoverflow`很棒**

使用 `stackoverflow`，整天搜索和问问题，把别人的答案看成福音，却没有去学习这些代码，短期效果好，长期是负效果。

**寻找有经验的帮助**

在刚入门的时候，看书自学，很容易感到沮丧和厌倦，基本上很浪费时间，并且收益不是很大。有经验的人，能直接找出你的不足，给你列出优先事项，节省时间和减少挫折感。


**制作自学环境**

作者自学的时候，把自己lock在图书馆和咖啡厅，减少外界的干扰。


**离开自己的世界出去认识人**

当你自学的时候，并不会有人去主动认识和寻找你，你需要自己展示自己。

&nbsp;

### 我的 `share`

**专注于过程**

我以前基本上也是结果导向的人，每次定 `todolist` 都是要完成什么什么，为了完成课程，对课程细节并没有深入理解，下次基本就是重学了。

**`Stackoverflow`很棒**

使用 `stackoverflow`，我已经很少用了，基本 `google`，但现在会尝试自己去把问题解决，即使知道答案在哪。

**寻找有经验的帮助**

这个备有感触，自己么，入门前两年基本是被虐过来的，虽然人家说我是专家，现在都不敢说自己入门了，不多说了。希望重新开始的时候，希望自己更加强大，处理好。


**制作自学环境**

我也是把自己 `lock` 在图书馆和咖啡厅，减少外界的干扰。在家基本没效率，去了这些地方，都是采用番茄工作法，但是还不够番茄，很多时候会被打扰。


**离开自己的世界出去认识人**

这个也算死结了，等人推荐吧，自己也不认识人。


&nbsp;

## Lecture

课程地址
[Machine Learning](https://github.com/rubust-ai/Machine-Learning)



课程地址 [Week9 Anomaly Detection](https://www.coursera.org/learn/machine-learning/home/week/9)

主要内容

**异常检测**
- 异常检测
- 高斯分布
- 高斯分布异常检测算法
- 异常检测实施
- 多元高斯分布

**推荐系统**

- 问题符号化
- 基于内容推荐
- 协同过滤
- 协同过滤算法
- 矢量化：低轶矩阵分解
- 实施细节：均值规范化


我的笔记

[week9 notes](https://github.com/rubust-ai/Machine-Learning/blob/master/week09.md)

&nbsp;

[Week10 Large Scale Machine Learning](https://www.coursera.org/learn/machine-learning/home/week/10)

**主要内容**

大数据梯度下降

- 大数据学习
- 随机梯度下降
- 小批量梯度下降
- 随机梯度下降收敛调试

前沿话题

- 在线学习
- map-reduce和数据平行运算


我的笔记

[week10 notes](https://github.com/rubust-ai/Machine-Learning/blob/master/week10.md)

&nbsp;

[Week11 Application Example: Photo OCR](https://www.coursera.org/learn/machine-learning/home/week/11)

**主要内容**
照片光学字符识别
- photo OCR的问题和pipeline
- 滑动窗的使用
- 数据扩增
- **上限分析**
    - 很重要，能节省很多时间去做最能提升模型的步骤

**我的笔记**

[week11 notes](https://github.com/rubust-ai/Machine-Learning/blob/master/week11.md)


[编程作业 homework](https://github.com/rubust-ai/Machine-Learning/tree/master/homework)


## 尾巴

本周是5.1假期，基本都是在图书馆度过，最后看完 `week9` 和完成所有编程作业，已经完成吴恩达的机器学习。其中比较难的是编程中的矩阵大小，矩阵相乘问题，有不少题都 `debug` 了很久。

昨天并且完成 `deeplearning.ai` 的第一门课 `Introduction to Tensorflow` (四周课程)，量不大，是 `google` 人讲的，适合有深度学习和机器学习基础的人看，否则别看，相关的还有三门 `tensorflow` 的课程。

不准备再进一步学习了，之后再决定要学什么，目前将决策树相关知识，深度学习，`NLP` 项目补一补，把`Introduction to Deep Learning` 完结。