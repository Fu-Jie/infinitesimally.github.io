---
# layout    : archive
title     : 生成重复的随机数
date      : 2018-09-23
categories: Statistics
# classes   : wide
# permalink : /one/
---
使用python和matlab生成重复的随机数,关键在于种子生成器.

## 使用`rng`函数

```matlab
>> rng(1)
>> rand

ans =

	0.4170

>> rand

ans =

	0.7203

>> rng(1)
>> rand

ans =

	0.4170
% 当指定了rng种子,则下一次执行随机函数的值是固定的,要想获得同样的随机数,固定种子即可.
% 同时要求设定了种子之后,只有接下来的一次有效
```
## 使用`RandomState`函数
```python
In [1]: import numpy as np

In [2]: s1=np.random.RandomState(1)

In [3]: s1.randn(5)
Out[3]: array([ 1.62434536, -0.61175641, -0.52817175, -1.07296862,  0.86540763])

In [4]: s2=np.random.RandomState(1)

In [5]: s2.randn(5)
Out[5]: array([ 1.62434536, -0.61175641, -0.52817175, -1.07296862,  0.86540763])
# 这里的RandomState也是一个保存种子生成器的实例，当使用同样的种子生成的随机数也是一样的。

In [6]: s2.randn()
Out[6]: -2.3015386968802827 # 可以看出来只能使用一次，第二次就不一样了

In [7]: s3=np.random.RandomState(1)
In [8]: s3.randn()
Out[8]: 1.6243453636632417 # 再次生成一个新实例，依然保存着状态。
```
