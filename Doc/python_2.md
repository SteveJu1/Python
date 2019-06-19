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

# input
a_input=input()
print(a_input)

