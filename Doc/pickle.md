pickle 是一个 python 中, 压缩/保存/提取 文件的模块
import pickle
a_dict = {'da': 111, 2: [23,1,4], '23': {1:2,'d':'sad'}}
# pickle a variable to a file
file = open('pickle_example.pickle', 'wb')
pickle.dump(a_dict, file)
file.close()
wb 是以写二进制的形式打开 ‘pickle_example.pickle’ 这个文件, 
然后 pickle.dump 你要保存的东西去这个打开的 file. 
最后关闭 file 你就会发现你的文件目录里多了一个 ‘pickle_example.pickle’ 文件, 
这就是那个字典了.

# pickle 提取
# reload a file to a variable
with open('pickle_example.pickle', 'rb') as file:
    a_dict1 =pickle.load(file)
print(a_dict1)

import pickle
files=open('pickle_example.pickle','rb')
a_dic=pickle.load(files)
print(a_dic)
