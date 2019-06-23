# Week12 06/16/2019


## Algorithm




**要求**


**思路**


**解答**


&nbsp;

## Tips

### `numpy`内积和外积

```python
import numpy as np

Y = np.array([[1 1 1]])
AL = np.array([[ 0.8  0.9  0.4]])

print(Y.shape)
print(np.dot(Y,AL.T))
print(np.dot(Y.T,AL))

# output
'''
(1, 3) # Y.shape
[[ 2.1]] # np.dot(Y,AL.T)
[[ 0.8  0.9  0.4] #np.dot(Y.T,AL)
 [ 0.8  0.9  0.4]
 [ 0.8  0.9  0.4]]
'''
```










&nbsp;
## Share



### 作者的`Share`

### 我的`Share`


&nbsp;
## Lecture

课程 `link`


[Neural Networks and Deep Learning](https://www.coursera.org/learn/neural-networks-deep-learning/home/week/3)

笔记 `link`

[Week1 Introduction to deep learning](https://github.com/rubust-ai/Deep-Learning/blob/master/class1-week3.md)


