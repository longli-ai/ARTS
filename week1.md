# Week1 03/31/2019

## Algorithm

### [344. Reverse String](https://leetcode.com/problems/reverse-string/)

题目要求
- 不能另外新建一个数组，只能用O(1)额外内存来修改数组
- 函数不需要返回，因为列表是就地更改

解题思路
- 核心就是交换列表前后项的值
- 开始采用while i<l/2的方法，结果显示时间超时
- 更改成for循环，时间没问题
- 开始采用c语言的tmp作为中间值传递进行交换，后来发现python可以直接交换
- 我的解法 [344_Reverse_String.py](https://github.com/longli-ai/Leetcode-python3/blob/master/344_Reverse_String.py)

### [922. Sort Array By Parity II](https://leetcode.com/problems/sort-array-by-parity-ii/)

题目要求

- 保持奇数位数字为奇数，偶数位为偶数

解题思路
- 第一步，选出输入列表的不正常的位置，并且记录到奇偶列表
- 第二步，合并奇偶列表，选取首尾进行输入列表的交换（上题）
- 可以遇见性的知道，内存占用会相对较大，速度应该还可以
- 我的解法 [922_Sort_Array_By_Parity_II.py](https://github.com/longli-ai/Leetcode-python3/blob/master/922_Sort_Array_By_Parity_II.py)

### [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)

题目要求

- 从已经排好序的列表中，就地删除列表中相同值元素

解题思路
- 排好序列表，去重，基本就是删除临近相同值的元素
- 核心倒序删除相同元素
- 在列表中，数字是有顺序的，正序删除会影响后续数字的index改变，所以倒序倒是一个万金油的方法
- 发现'nums.pop(i)'速度比'del nums[i]'要慢4ms
- 我的解法  [026_Remove_Duplicates_from_Sorted_Array.py](https://github.com/longli-ai/Leetcode-python3/blob/master/026_Remove_Duplicates_from_Sorted_Array.py)

[80. Remove Duplicates from Sorted Array II](https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/)

题目要求

- 第一次做中等难度，但解法和上题目基本相同

解题思路
- 核心倒序删除
- 判断三个相邻数字，是否相同，相同删除当前数字，并且不会影响前面数字在列表中的index，如果正序删除，则会影响后面数字在列表中index
- 我的解法 [080_Remove_Duplicates_from_Sorted_Array_II.py](https://github.com/longli-ai/Leetcode-python3/blob/master/080_Remove_Duplicates_from_Sorted_Array_II.py)

## Review
### [Chapter 2 : SVM (Support Vector Machine) — Theory](https://medium.com/machine-learning-101/chapter-2-svm-support-vector-machine-theory-f0812effc72)

主要内容

- 其主要内容对于我们进行 svm 炼丹(tuning parameters)有比较大的帮助. 学了其他课程的svm理论知识，他这篇的“理论”，结合sklearn，实现code层面的炼丹. 

## Tips
这周折腾安装ubuntu/cuda/cudnn/tensorflow时候，感觉坑很多。目前还没安装完，很耗费时间，之后准备根据自己的note，写一个csh，以后装完ubuntu，直接执行csh，让它自己安装，尽量少手动。此外还有docker，还没学，学完字后直接用docker就可以了。

首当其冲就是下载，在用apt下载时候，无论什么source，都很慢，需要挂代理，由于ubuntu还没配置ss，用Mac去下载cuda/source/cudnn/nv driver，然后通过NAS给ubuntu

```shell
# how to solve apt-get 下载速度慢
# use Macbook download sources, then copy it in
sudo cp xxx.deb /var/cache/apt/archives/
```
pip的source，用豆瓣pip下载速度飞起
```shell
mkdir ~/.pip/

# add following code in ~/.pip/pip.conf
[global]
trusted-host = pypi.douban.com
index-url = http://pypi.douban.com/simple
```

## Share
### [Github 996ICU](https://github.com/996icu/996.ICU)

过去一周，最火的github项目，就是国内人开的996ICU，目前已经120k+ stars，其中有些人想要求开源组织，更改其协议，996黑名单公司，不准使用开源代码。

我所在的公司，是外企，基本算是965，大部分工种平时也很少加班，一般不会周六周日加班，有些工种会加班，基本对外客户的，需要及时解决客户问题，收入相对于其他工种也较高一些，这也是大家能接受的。公司本身是反对加班，我们公司的文化认为，如果持续加班，一般会是两个问题，第一经理派活过多，这样经理会被自己的经理review的。第二个就是工程师的水平不够，一般来说需要让经理去检查工程师的干活效率，帮助其成长，如果工程师能力实在不够，会辞退。每次高层次的经理和我们对话，都会问work-life balance的问题，问工作生活上有什么困难他们能帮我们解决的。

首先加班是违法的，违法的，违法的。
大厂和小企之间，不少大厂基本实行965，尤其有劳权的外企，政府会倾向于保护劳动者权益。这些大厂有资源，基本看小企业成功就买掉，补充自己的不足。小企为了和大厂或者其他的小企业竞争，基本就有了加班的问题了，前期不加班基本企业会死掉，但基本也会给予前期员工很多许诺，员工也有动力加班。
企业和员工之间，在目前的国情下，员工在企业面前基本就是被殴打的。企业就是就是为了最大化利润，本能反应压榨员工，员工也没啥反抗余地。其归根到底的原因，除企业和员工以外的第三方不作为，导致违法的行为没有被制止。

无约束条件下，企业连法都敢违，还害怕开源协议？


