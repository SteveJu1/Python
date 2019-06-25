# Python
 ### 安装
  * [Windows下Python环境的安装（Anaconda+Jupyter notebook+Pycharm）](https://zhuanlan.zhihu.com/p/59027692)
 
## [基础知识](https://github.com/lukkyy/Python/blob/master/Doc/%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86.md)

## Numpy & Pandas 
* 应用：数据分析.机器学习.深度学习
* 优点：1）运算速度快：numpy 和 pandas 都是采用 C 语言编写, pandas 又是基于 numpy, 是 numpy 的升级版本。
        2）消耗资源少：采用的是矩阵运算，会比 python 自带的字典或者列表快好多
* 安装
 pip3 install numpy/sudo apt-get install python-numpy
* 使用 
import numpy as np #为了方便使用numpy 采用np简写
* 属性
```
ndim：维度 
shape：行数和列数 
size：元素个数
```
```python
array = np.array([[1,2,3],[2,3,4]])
array.ndim
```
