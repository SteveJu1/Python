### python中的axis

axis用来指明将要进行的运算是沿着哪个轴执行，
在 numpy 中， 0 轴是垂直的，也就是列，而 1 轴是水平的，也就是行。
例如：
A=[[1,2,3]
   [4,5,6]
   [7,8,9]]
A.sum(axis = 0)表示A中的列相加
>>> print(A.sum(axis = 0))
>>> [12,15,18]

#### broardcasting 广播机制
A=[[1,2,3]
   [4,5,6]
   [7,8,9]]
B= 2
计算A除以B，通常可以写成A/B.reshape(1,3)，reshape时间复杂度是o(1)
直接写成A/B的话，broardcasting先将B变成1 × 3维的矩阵
B=[[2]
   [2] 
   [2]]
然后在相除
broardcasting：如果两个数组的有一个维度相等，另一个维度有一个数组的轴长度为 1，则认为它们是广播兼容的。  
广播会在缺失维度和轴长度为 1 的维度上进行。
```
a = np.random.randn(5)，这样会生成数组a中的 5 个高斯随机数变量。
a.shape是一个(5, )的结构。这在 Python 中被称作一个一维数组
不建议这样做，
```
AxB运算和numpy.dot(A, B)有什么不同：  
x运算是元素逐一相乘（element wise），而numpy.dot则是数学上的矩阵乘法运算
