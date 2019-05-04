# Week5 04/28/2019

### GitHub公式显示插件
Github 的 markdown 不支持数学公式, 安装下面的 chrome 安装 mathjax 插件，可以正常看 markdown 文中的数学公式，当然前提是你需要过墙，才能安装。


[Github with mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)


## Algorithm

[189. Rotate Array](https://leetcode.com/problems/rotate-array/)

**题目要求**
- 给定一个列表和一个k
- 对列表进行元素轮转，将最后一个元素搬到最前面，进行k轮

**解题思路**
- 由于看的实例，所以直接认为$k < len(nums)$
- 想采用for循环，但是速度不行
- 比较快的方法：将$nums$后面的k个元素就地直接调换到最前面
- 然后提交，发现了$k > len(nums)$特例
- 当$k > len(nums)$， 其实对于列表循环结果结果来说$k = k % len(nums)$

**我的解法**

[189_Rotate_Array.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/189_Rotate_Array.py)




## Tips

看这几篇文档就够了

[Git的奇技淫巧](https://github.com/521xueweihan/git-tips)

[git - 简明指南](http://rogerdudler.github.io/git-guide/index.zh.html)

[git 小抄](http://rogerdudler.github.io/git-guide/files/git_cheat_sheet.pdf)

**上传至 Github，实用**

```bash
git init # 本地初始化仓库
git add . # 本地添加所有文件
git commit -m "initial" # 本地提交仓库
git remote add origin https://github.com/rubust-ai/git_learning.git  # 将本地代码关联到github上
git pull origin master  # 上传代码到github之前，需要要更新你的本地仓库至最新改动
git push -u origin master # 上传代码到远程git仓库

# 输入用户名密码即可 push 入 github master branch
```


## Share

本周分享的是下面这篇文章，也是方法论相关，每周都给自己打鸡血。

[Why you learn the most when you feel like you’re struggling as a developer](https://medium.freecodecamp.org/why-you-learn-the-most-when-you-feel-like-youre-struggling-as-a-developer-7513327c8ee4)

开发过程中难免会遇到挫折，当我们继续前行，我们会发现我们在挫折中学到更多。


## Lecture

[CS229 Stanford Machine Learning(On-going)](https://github.com/rubust-ai/CS229-Machine-Learning)

[Week7 Support Vector Machines](https://www.coursera.org/learn/machine-learning/home/week/7)

主要内容


大间距分类器
- 优化目标
- 大间距直观展示
- 大间距背后的数学推导

核函数
- 内核的意义

SVM实战
- 线性内核
- 高斯内核
- 多分类
- 模型选择

我的笔记

[week7 notes](https://github.com/rubust-ai/CS229-Machine-Learning/blob/master/week07.md)

&nbsp;
[Week8 Unsupervised Learning](https://www.coursera.org/learn/machine-learning/home/week/8)

主要内容

聚类定义
K-means算法
- 算法流程
- 目标优化算法
- 存在问题
- 怎样选择K


降维
- 数据压缩
- 数据可视化

主成分分析算法
- 算法流程
- 和线性回归的相似和不同之处

pca实施
- 数据预处理
- 求解奇异方程
- 保持数据差异性(99%)
- 怎样选择k


我的笔记

[week8 notes](https://github.com/rubust-ai/CS229-Machine-Learning/blob/master/week08.md)

&nbsp;

