外部模块就是在你 import 什么东西去python 脚本的时候会用到的.
import numpy as np
 * 安装/卸载
 pip install numpy   # 这是 python2+ 版本的用法
 pip3 install numpy   # 这是 python3+ 版本的用法
 pip3 uninstall numpy
 
 * 更新外部模块
 pip3 install -U numpy

写文件
file=open('my_file.txt','w') #'w'=write 'a'=append
file.write('eat apple')
file.close()

读文件
file=open('my_file.txt','r') 'r'=read
content=file.read()
content=file.readlines()
print(content)

class 类
class Calculator: 推荐以大写的形式定义
	name='Tom'
	price=18    #属性
	def add(self,x,y): #功能
		print(self.name)
		result=x+y
		print(result)
#调用类		
cal=Calculator()
print(cal.name)
#__init__可以理解成初始化class的变量，取自英文中initial 最初的意思
class Calculator:
    def __init__(self, name, price):
        self.name = name
        self.pri = price
cal=Calculator('t',10)
print(cal.name)
print(cal.pri)#
如何设置属性的默认值, 直接在def里输入即可，如下:

def __init__(self,name,price,height=10,width=14,weight=16):查看运行结果， 三个有默认值的属性，可以直接输出默认值，这些默认值可以在code中更改, 比如c.wi=17再输出c.wi就会把wi属性值更改为17.同理可推其他属性的更改方法。

# input
a_input=input()
print(a_input)

