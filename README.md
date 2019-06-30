# Python
 ### 安装
  * [Windows下Python环境的安装（Anaconda+Jupyter notebook+Pycharm）](https://zhuanlan.zhihu.com/p/59027692)
 
### [Python基础知识汇集](https://github.com/lukkyy/Python/blob/master/Doc/%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md)  
```python
本地下载网上的数据
import tensorflow as tf
zip_file = tf.keras.utils.get_file(origin="https://storage.googleapis.com/mledu-datasets/cats_and_dogs_filtered.zip",
                                   fname="cats_and_dogs_filtered.zip", extract=True)    #下载数据并解压
[参考](https://github.com/tensorflow/docs/blob/master/site/en/tutorials/images/transfer_learning.ipynb)
```
    
### Numpy & Pandas 
___
#### 应用：数据分析.机器学习.深度学习
#### 优点：
* 1）运算速度快：numpy 和 pandas 都是采用 C 语言编写, pandas 又是基于 numpy, 是 numpy 的升级版本。
 * 2）消耗资源少：采用的是矩阵运算，会比 python 自带的字典或者列表快好多
#### 安装
 pip3 install numpy/sudo apt-get install python-numpy
#### 加载numpy 
```
import numpy as np  #为了方便使用numpy 采用np简写
```
#### 创建 array 
```
# array：创建数组        
a = np.array([2,23,4]) 
# dtype：指定数据类型    
a = np.array([2,23,4],dtype=np.int)
print(a.dtype)
# int 64

# zeros：创建数据全为0
a = np.zeros((3,4))    # 数据全为0，3行4列

# ones：创建数据全为1
a = np.ones((3,4))     # 数据为1，3行4列

# empty：创建数据接近0

# arange：按指定范围创建数据 
a = np.arange(10,20,2) # 10-19 的数据，2步长

#使用 reshape 改变数据的形状
a = np.arange(12).reshape((3,4))    # 3行4列，0到11
"""
array([[ 0,  1,  2,  3],
       [ 4,  5,  6,  7],
       [ 8,  9, 10, 11]])

# linspace：创建线段
a = np.linspace(1,10,20)    # 开始端1，结束端10，且分割成20个数据，生成线段
"""
array([  1.        ,   1.47368421,   1.94736842,   2.42105263,
         2.89473684,   3.36842105,   3.84210526,   4.31578947,
         4.78947368,   5.26315789,   5.73684211,   6.21052632,
         6.68421053,   7.15789474,   7.63157895,   8.10526316,
         8.57894737,   9.05263158,   9.52631579,  10.        ])
"""

np.expand_dims:用于扩展数组的形状
a = np.array([[[1,2,3],[4,5,6]]])
>>> a.shape #(1, 2, 3)
>>> b = np.expand_dims(a, axis=0)  #axis=0,1h好像是一样的结果
# array([[[[1, 2, 3],
         [4, 5, 6]]]])
 >>>  np.expand_dims(a, axis=2)  
# array([[[[1, 2, 3]],
        [[4, 5, 6]]]]) #(1, 2, 1, 3)
```

#### 属性
```
# ndim：维度 
# shape：行数和列数 
# size：元素个数
array = np.array([[1,2,3],[2,3,4]])
print(array.ndim)
```
#### 功能

##### 分割
```
A = np.arange(12).reshape(3, 4)
[[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]
# 纵向分割, 分成两部分, 按列分割
print np.split(A, 2, axis = 1)
[array([[0, 1],[4, 5],[8, 9]]), array([[ 2, 3],[ 6, 7],[10, 11]])]
# 横向分割, 分成三部分, 按行分割
print np.split(A, 3, axis = 0)
[array([[0, 1, 2, 3]]), array([[4, 5, 6, 7]]), array([[ 8, 9, 10, 11]])]

 不均等分割
print np.array_split(A, 3, axis = 1)

[array([[0, 1],[4, 5],[8, 9]]), array([[2],[6],[10]]), array([[3],[7],[11]])]
```
___
