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

