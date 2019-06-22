# Python
 ### 安装
  * [Windows下Python环境的安装（Anaconda+Jupyter notebook+Pycharm）](https://zhuanlan.zhihu.com/p/59027692)
 
### 基础知识
* 键盘输入或输出
```Python
a_input=input()
print(a_input)
```
* 写文件
```Python
file=open('my_file.txt','w') #'w'=write 'a'=append     #打开文件，若没有文件会新建一个文件
file.write('eat apple')                                #写入文件      
file.close()                                           #关闭文件
```
* 读文件
```Python
file=open('my_file.txt','r') #'r'=read
content=file.read()
content=file.readlines()
print(content)
```
###数据类型 （list、 tuple 、dict 和 set ）
### 元组, 列表, 字典
* List，列表是一系列有序的数列
添加 
```python
  a = [1,2,3,4,1,1,-1]
  a.append(0)    # 在a的最后面追加一个0
  print(a)      # [1, 2, 3, 4, 1, 1, -1, 0]
```
在指定的地方插入项：
```python
a = [1,2,3,4,1,1,-1]
a.insert(1,0)     # 在位置 1处添加0
print(a)          # [1, 0, 2, 3, 4, 1, 1, -1]
```

删除项：
```python
a = [1,2,3,4,1,1,-1]
a.remove(2)         # 删除第一个出现值为2的项
print(a)
# [1, 3, 4, 1, 1, -1]
```
索引 
```python
a = [1,2,3,4,1,1,-1]
print(a[0])  # 显示列表a的第0位的值
# 1

print(a[-1]) # 显示列表a的最末位的值
# -1

print(a[0:3]) # 显示列表a的从第0位 到 第2位(第3位之前) 的所有项的值
# [1, 2, 3]

print(a[5:])  # 显示列表a的第5位及以后的所有项的值
# [1, -1]

print(a[-3:]) # 显示列表a的倒数第3位及以后的所有项的值
# [1, 1, -1]

打印列表中的某个值的索引(index): a.index
a = [1,2,3,4,1,1,-1]
print(a.index(2))     # 显示列表a中第一次出现的值为2的项的索引
# 1

统计列表中某值出现的次数：a.count
a = [4,1,2,3,4,1,1,-1]
print(a.count(-1))
# 1
```
List 排序 ：a.sort / a.sort(reverse=True)

```python
a = [4,1,2,3,4,1,1,-1]
a.sort() # 默认从小到大排序
print(a)
# [-1, 1, 1, 1, 2, 3, 4, 4]
a.sort(reverse=True) # 从大到小排序
print(a)
# [4, 4, 3, 2, 1, 1, 1, -1]
```
***

### Set() 
寻找一个句子或者一个 list 当中不同的元素
```python
char_list = ['a', 'b', 'c', 'c', 'd', 'd', 'd']
sentence = 'Welcome Back to This Tutorial'
print(set(char_list)) # {'b', 'd', 'a', 'c'}
print(set(sentence)) # {'l', 'm', 'a', 'c', 't', 'r', 's', ' ', 'o', 'W', 'T', 'B', 'i', 'e', 'u', 'h', 'k'}

print(set(char_list+ list(sentence)))     #相加的话先把字符串变为List
# {'l', 'm', 'a', 'c', 't', 'r', 's', ' ', 'd', 'o', 'W', 'T', 'B', 'i', 'e', 'k', 'h', 'u', 'b'}
```

添加元素 
定义好一个 set 之后我们还可以对其添加需要的元素, 使用 add 就能添加某个元素. 但是不是每一个东西都能添加, 比如一个列表.
```python
unique_char = set(char_list)
unique_char.add('x')
# unique_char.add(['y', 'z']) this is wrong
print(unique_char)
# {'x', 'b', 'd', 'c', 'a'}
```
清除一个元素可以用 remove 或者 discard, 而清除全部可以用 clear.
```python
unique_char.remove('x')
print(unique_char)
# {'b', 'd', 'c', 'a'}

unique_char.discard('d')
print(unique_char)
# {'b', 'c', 'a'}
unique_char.clear()
print(unique_char)
# set()
```


* List，列表是一系列有序的数列
  a = [1,2,3,4,1,1,-1]

# tuple(元组)
tup = ('python', 2.7, 64)
for i in tup:
    print(i)
    
# dictionary
dic = {}
d={'a':1,'ga':s}
print(d['a'])
del d['a']
d['s']=10
dic['lan'] = 'python'
dic['version'] = 2.7
dic['platform'] = 64
for key in dic:
    print(key, dic[key])
    



### while 和 for 循环

### if 判断

### 函数
```Python 
def fun():             #先定义函数
    print('This is a function')
    a = 1+2
    print(a)
fun()                  #调用函数
```Python

 # define a Fib class
class Fib(object):
    def __init__(self, max):
        self.max = max
        self.n, self.a, self.b = 0, 0, 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.n < self.max:
            r = self.b
            self.a, self.b = self.b, self.a + self.b
            self.n = self.n + 1
            return r
        raise StopIteration()

# using Fib object
for i in Fib(5):
    print(i)
    
def fun()
  global a
after run fun() a=global a 

var = var1 if condition else var2
x=4
y=5
z = x if x>1 else y
print(var)



### 定义class类
```Python
# 先定义
class Calculator:      # class类推荐以大写的形式定义
	name='Tom'
	price=18              #属性
	def add(self,x,y):    #功能/函数
		print(self.name)
		result=x+y
		print(result)
# 在调用类		
cal=Calculator()
print(cal.name)

#初始化class的变量
#__init__取自英文中initial 最初的意思
class Calculator:
    def __init__(self, name, price):
        self.nam = name
        self.pri = price
cal=Calculator('t',10)
print(cal.nam)
print(cal.pri)
...
t
10
...
# 设置属性的默认值, 直接在def里输入即可
def __init__(self,name,price,height=10,width=14,weight=16):
更改默认值 比如c.wi=17再输出c.wi就会把wi属性值更改为17
```

### 加载模块

import time
print(time.localtime)
import time as t
print(t.localtime)
from time import localtime
localtime()
from time import *

# 自己创建的模块
在同一目录下 myPython.py
import myPython
myPython.func

break 跳出 
continue 



模块就是在你 import 什么东西去python 脚本的时候会用到的.
 * 加载模块
 ```
 import numpy as np
 ```
 * 安装/卸载/更新模块
 ```
 pip install numpy   # 这是 python2+ 版本的用法
 pip3 install numpy   # 这是 python3+ 版本的用法
 pip3 uninstall numpy
 pip3 install -U numpy # 更新外部模块
 ```
### try except
```
try:
    file = open('eeee', 'r+')   #r+ read and add
except Exception as e:                   #Exception为默认函数
    print('there is no file named as eeeee')
    response = input('do you want to create a new file')
    if response =='y':
        file = open('eeee','w')
    else:
        pass
else:
    file.write('ssss')
file.close()
```
***

### 正则表达式 (Regular Expression) 
又称 RegEx, 是用来匹配字符的一种工具. 在一大串字符中寻找你需要的内容. 
它常被用在很多方面, 比如网页爬虫, 文稿整理, 数据筛选等. 
最简单的一个例子, 比如我需要爬取网页中每一页的标题. 而网页中的标题常常是这种形式.
<title>我是标题</ title>
