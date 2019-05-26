# Week8 05/19/2019

## GitHub公式显示插件
Github 的 markdown 不支持数学公式, 安装下面的 chrome 安装 mathjax 插件，可以正常看 markdown 文中的数学公式，当然前提是你需要过墙，才能安装。

[Github with mathjax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)

&nbsp;
## Algorithm

**题目**
[942. DI String Match](https://leetcode.com/problems/di-string-match/)

**要求**
- `S`的所有元素都是`D`和`I`
- `A`是`[0,...,len(S)]`
- `If S[i] == "I", then A[i] < A[i+1]`
- `If S[i] == "D", then A[i] > A[i+1]`


**思路**
- 上来感觉答案不唯一，经过观察例子，发现所有`D`，其实都是倒序的数字，所有`I`都是顺序的数字
- 经过采用创建数字列表，进行`remove`元素到输出，有个测试的例子很长，发现时间超
- 采用常规`l,r`的做法，避免无意义的操作，免去生成数字列表，再`remove`。

**解答**

[942_DI_String_Match.py](https://github.com/rubust-ai/Leetcode-python3/blob/master/942_DI_String_Match.py)


&nbsp;
## Tips

```python
RANGE_NUM = 100

# 第一种方法：对列表进行迭代
for i in [x*x for x in range(RANGE_NUM)]: 
    # do sth for example
    print(i)
        
# 第二种方法：对generator进行迭代
for i in (x*x for x in range(RANGE_NUM)): 
    # do sth for example
    print(i)
```

这俩`for`循环其实是有区别的，第一个是列表循环，第二个是迭代器循环。

其中计算资源表现的话，迭代器的效果要比列表要好。列表上来把所有数字全做了平方，存入内存中，其内存占用比较高。
而迭代器用多少，取出来计算，返回，挂起来等待下次调用。相对来说也省计算资源。


&nbsp;
## Share

本周分享 [We Don’t Need Social Media](https://onezero.medium.com/we-dont-need-social-media-53d5455f4f6b)

**作者的`Share`**

`facebook`的联合创始人提出分拆社交媒体。认为联合创始人提出的做法这是很鸡贼，仅仅是为了孵化自己或者他人的小企业，而忽略了社交媒体的弊大于利。

作者认为不需要社交媒体来帮助企业和国家监督我们的生活。不需要社交平台的骚扰和跟踪。我们不需要它来传播阴谋和暴力。我们也不需要它来毒害我们的民主话语或用危险的反科学无稽之谈来感染我们的思想。

**我的`Share`**

其实我一直很反感社交媒体，认为社交媒体其实不应该嵌入我们的生活，整个社会的氛围已经被社交媒体带的很浮躁。比如微信已经嵌入我们的工作，别人找你，你需要很快的回复，并且根本没有电话和邮件效率来的高，只能算回复及时。

我一直认为人人应该过上 `life-work balance`。当你工作就是在工作，电话，邮件，开会，这些都不是问题。但当你生活的时候，很多时候会被工作的事情打扰，需要你尽快回复，很多公司都给员工配置链接公司的`vpn`，其目的不仅仅希望员工能远程工作，重要的是能及时处理问题。

```“Some days, lying on the floor next to my 1-year-old son, I catch myself scrolling through Instagram, waiting to see if the next image will be more beautiful than the last,” he wrote.```

为什么我们经常不会不停的刷照片，上面是社交激励的一个例子，比如刷微博抖音看妹子。手指不停的刷，不停的期待，直到看到漂亮的妹子，给你我带来一个愉悦的感觉，得到这样的奖赏。这个和耗子叔说的一致，我们在被抖音微信微博这些社交平台**消费**。





&nbsp;
## Lecture

课程链接 [Recurrent Neural Networks](https://www.coursera.org/learn/nlp-sequence-models/home/week/1)


笔记链接 [week1 Recurrent Neural Networks](https://github.com/rubust-ai/Deep-Learning/blob/master/class5-week1.md)


&nbsp;
## 尾巴

世界开始动荡了，华为被禁只是一个贸易战开始，宗教战争也不会太远。这时候强大我自己才能站稳脚跟，多赚点保值的东西。

本周由于 `BTC` 的暴涨暴跌，导致我有些激动，还开了合约，基本没心情学习，需要常看手机。对自己我还是那个说法，只屯 `BTC`和黄金，不问涨跌，不管以后是穷还是富有，保证自己一直在屯即可。现阶段虽然整个世界还算安定，但是明显冲突的可能越来越大。希望预备我们这代人用不到。

说实话，`ARTS`我都有点想放弃了，想想还是不能放弃，毕竟还是想坚持20周的。

今天把算法题做了，但是课程还没填完笔记。精力在币圈，没有投入过多的学习精力，从这几天开始要开始自救，继续学习。


