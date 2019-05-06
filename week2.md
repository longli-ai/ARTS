# Week2 04/07/2019


## Algorithm

### [867. Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)

题目要求
- 将矩阵进行转置，就是将$A$矩阵的$A_{18}$转化成$A_{81}$
- 将$m * n$转置成 $n * m$
- python的numpy中有专门的专置函数($A.T$)

解题思路
- 首先计算新的矩阵的行数，即n是多大
- 然后根据n创建n个空的列表
- 然后进行for循环，将每个row中的数字push到上面的相应列表中
- 看了下标准解法，基本相同
- 我的解法 [867_Transpose_Matrix.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/867_Transpose_Matrix.py)

### [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)

题目要求
- 这题目就是让判断括号这种符合不符合语法
- 这个题目应该面试比较火的题目



解题思路1

- 使用不停去除已经配对的括号
- ```s = s.replace('{}', '')```

- 当余下的值不在变化的时候，就是停止的时候
- 我的解法 [020_Valid_Parentheses.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/020_Valid_Parentheses.py)



解题思路2

- 通过stack的思想，先入后出，把list当stack来用
- 将元素一个个append到stack中，每次append之前，查一下和list最后一个元素组成对么
- 组成对，就pop，否则继续append进去
- 最后检查一下stack(list)的大小是否为0
- 我的解法 [020_Valid_Parentheses2-stack.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/020_Valid_Parentheses2-stack.py)


## Tips






### python的zip函数
```python
X = [[1,2,3],[4,5,6,7]]
print(zip(*X)) # *X是将X进行解压，本例子中解压成两个list，即[1,2,3]和[4,5,6,7]
# zip(*X)是对上面两个list进行拉链，生成三个元组(1,4),(2,5),(3,6)
print(list(zip(*X))) # 重新将zip对象转化成list
```
输出
```output
<zip object at 0x10375e4c8>
[(1, 4), (2, 5), (3, 6)]
```

灵活使用zip函数，还是很便利的，比如上面的leetcode题目矩阵转置 [867. Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)
```python
return list(zip(*A))
```



不仅仅是list，string也可以，下面这个例子貌似也是leetcode的题目

```python
nums = ['flower','flow','flight']
for i in zip(*nums):
    print(i)
```

输出(由于string长度不一样，所以丢掉长的部分，没组成tuple)

```python
('f', 'f', 'f')
('l', 'l', 'l')
('o', 'o', 'i')
('w', 'w', 'g')
```



## Share

### [Why Did I Reject a Data Scientist Job?](https://towardsdatascience.com/why-did-i-reject-a-data-scientist-job-f2e56117fdae?nsukey=6RLs3xUBCGr6Kzp9hb%2FTrG3mUoHOhHim1kNIo4B3pEskltlagEthldMeXtr0CZDK4ESJk95DyhCTzmaybMzT15L3r%2FOMgCoCwPmnmkXYqb4m3IRqdlU7RwwTOSbxEaedueA0eS%2FxS%2Fun1lGmSdyl63PS1UTky3SQMh%2F0Cgj0cdDL5gT8GMnhD3XELqBeCeTsISRm1vfxEWHakiTFLU5n5A%3D%3D)

最重要一点就是区分 Job Title ≠ Job Nature
- Job Title
    - 工作的职称是啥，比如 Java 工程师，机器学习工程师
    - 其实质是技能 skill
- Job Nature
    - 做啥，工作内容实质是啥，需要啥技能

其实我的想法和作者有些相似，一直以来就是所谓的工程师思想
- 其实你并不需要知道你的工作职称是啥。你需要知道你要完成啥，怎么能把它完成，必要手段就是切分成一个个小目标，使用什么**技能**（可以说就是我们的 skill ）把这些小目标一点点完成。
- 所以你知道自己是做啥的，不需要强调自己的 skill title.




## Lecture


[Machine Learning Week1](https://www.coursera.org/learn/machine-learning/home/week/1)

主要内容

- 机器学习定义，解决问题（回归和分类），监督学习定义，无监督学习定义
- 线性回归模型，其损失函数，相关线性代数

- 我的笔记 [week1 notes](https://github.com/rubust-ai/Machine-Learning/blob/master/week01.md)

[Machine Learning Week2](https://www.coursera.org/learn/machine-learning/home/week/2)

主要内容

- octave的安装，多变量线性模型，特征幅度缩放，特征归一化，学习率的选择，正规函数（矩阵求解$\theta$),
- octave的使用，作业题目是手写 **梯度下降**，值得注意的区分就是$X'*\theta$还是$\theta*X$
- 切记：octave与其他的语言不同，采用1-n到多少，其他语言基本都是0-n，比如矩阵A[:,1:2]代表第1列，第2列

- 我的笔记 [week2 notes](https://github.com/rubust-ai/Machine-Learning/blob/master/week02.md)




### 本周尾巴

上周开始有想法改变ARTS的分享内容，想将ARTS和自己的学习相结合，感觉有些和自己的平时学习相悖，毕竟时间还是有些冲突的。目前把其中review的部分目前改成学习外国精品课程(Lecture)，以后或许改成ARTSL，其L代表lecture，即每周学习一周精品课程，但量有些大，很难坚持，目前去除R，反正都是英文的。
