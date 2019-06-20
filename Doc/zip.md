# zip
zip函数接受任意多个（包括0个和1个）序列作为参数，合并后返回一个tuple列表,请看示例：
```python
a=[1,2,3]
b=[4,5,6]
ab=zip(a,b)
print(ab)
"""
<zip object at 0x000000000C871D08>
"""
print(list(ab))  #需要加list来可视化这个功能
"""
[(1, 4), (2, 5), (3, 6)]
"""
```
```python
# lambda
fun = lambda x,y:x+y
x=input()
y=input()
print(fun(x,y))
"""
x=2
y=2
22
"""
fun = lambda x,y:x+y
x=int(input('please input x='))  #默认输入为字符串，这里要转成int整数，
y=int(input())
print(fun(x,y))
"""
x=2
y=2
4
"""
```
