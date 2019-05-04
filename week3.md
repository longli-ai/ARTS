# Week3 04/14/2019



### GitHub公式显示插件
github 的 markdown 不支持公式, 安装下面的 chrome 安装插件，可以正常看 markdown 文中的公式，当然前提是你需要过墙。

[github with mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)


## Algorithm

### [561. Array Partition I](https://leetcode.com/problems/array-partition-i/)

题目要求
- 将$2n$正整数排列成两两整数元组的形式，每个元组求最小值
- 然后将最小值加起来，求最大值输出

解题思路
- 首先是如果是一个有序数列，所有值中最大的最小值是多少，肯定是倒数第2个数，并且要最大值组队，求最小才能得到。
- 依次向前，可以发现有序数列的偶数位的数字就是我们要找的。
- 有点背包问题的味道
- 我的解法 [561_Array_Partition_I.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/561_Array_Partition_I.py)
- 别人的解法
    - 直接切片sorted之后的数组，list这操作厉害

```python3
        return sum(sorted(nums)[::2])
```

## Tips

更换教程，上次教程太差了，还是老外写的给力，不吹不黑。

[git - 简明指南](http://rogerdudler.github.io/git-guide/index.zh.html)


一直使用github的desktop版本，内部command都没用，平时只会click两个buttons😓
- 'Commit to master'和'push origin'

**部分简单command**
```bash
git init #初始化一个git仓库
git add <file> #添加文件
git commit -m <message> #给这次更新加comment
git log #查看提交历史
git reset --hard <commit_id> #切换版本
git reset --hard HEAD^ #向后1步，切换版本
git reflog #查看命令历史，可以还原当前HEAD之前的版本
git status #查看当前工作区，有没有文件被更改或添加
```

**HEAD移动，代表版本的移动**
![](https://user-images.githubusercontent.com/41643043/56090262-86401300-5ed2-11e9-9a65-6705f4b86516.png)

**git的实际操作**

把文件往git版本库里添加的时候，是分两步执行的：
- 第一步是用git add把文件添加进去，实际上就是把文件**修改**添加到暂存区；
- 第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。
![rep_file](https://user-images.githubusercontent.com/41643043/56090449-e89a1300-5ed4-11e9-878d-1e5622ba6d3c.jpeg)

下周继续学习pull，push，merge，rebase这些命令




## Share

### [What I’ve learned six months into my first job as a self-taught software engineer](https://medium.freecodecamp.org/what-ive-learned-six-months-into-my-first-job-as-a-self-taught-software-engineer-516b0703e86)

内容是作者从一个自学成才的软件设计师，进入公司6个月内生活和建议。



## Lecture
### [Stanford Machine Learning Week3](https://www.coursera.org/learn/machine-learning/home/week/3)

主要内容 逻辑回归和正则化

- 分类算法，假设函数sigmoid，决策边界
- 分类条件下损失函数，简化损失函数log function，梯度下降以外的高级优化
- 逻辑回归的多分类one-vs-all

- 欠拟合，过拟合在样本中损失函数和学习曲线表现形式
- 解决过拟合的方法，减少特征数量和正则化
- 正则化的核心思想，采用更简单的假设函数去预测模型
- 线性回归的正则化损失函数
- 逻辑回归的正则化损失函数

- 我的笔记 [week3 notes](https://github.com/rubust-ai/CS229-Machine-Learning/blob/master/week03.md)

### [Stanford Machine Learning Week4](https://www.coursera.org/learn/machine-learning/home/week/4)

主要内容

- 神经网络的动机：非线性假设函数
- 神经元结构，activation和weights的层数相关定义，weights矩阵的大小
- 前向传播的公式
- 实例：为什么神经网络能学习复杂的非线性假设
    - not/and/or/xnor/xor的实现
- 神经网络的多分类
    - one-vs-all

- 我的笔记 [week4 notes](https://github.com/rubust-ai/CS229-Machine-Learning/blob/master/week04.md)




### 尾巴
本周新鲜事，将 arts 和 Stanford machine learning notes 都直接用github来管理，采用 Mweb 和 typora 来写这些文档，写好，打开github，点击'Commit to master'和'push origin'，然后就能在github上看到了，并且隔天手机 PPhub 上还能看到绿色的砖块，显示前一天的工作勤奋度。