# Python
 ### 安装
  * [Windows下Python环境的安装（Anaconda+Jupyter notebook+Pycharm）](https://zhuanlan.zhihu.com/p/59027692)
 
### 基础知识
* 键盘输入
```Python
a_input=input()
print(a_input)
```
* 写文件
```Python
file=open('my_file.txt','w') #'w'=write 'a'=append
file.write('eat apple')
file.close()
```
* 读文件
```Python
file=open('my_file.txt','r') #'r'=read
content=file.read()
content=file.readlines()
print(content)
```
### while 和 for 循环

### if 判断

### 定义函数

### 定义class类
```
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

### 元组, 列表, 字典

### 正则表达式 (Regular Expression) 
又称 RegEx, 是用来匹配字符的一种工具. 在一大串字符中寻找你需要的内容. 
它常被用在很多方面, 比如网页爬虫, 文稿整理, 数据筛选等. 
最简单的一个例子, 比如我需要爬取网页中每一页的标题. 而网页中的标题常常是这种形式.
<title>我是标题</ title>
