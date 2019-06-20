什么是id？一个对象的id值在Python解释器里就代表它在内存中的`地址`
copy shadow copy 和 deep copy
a=[1,2,3]
b=a 
id(a)==id(b) 索引相同，改变a或b的值，另一方同时改变
# shadow copy
import copy
a=[1,2,3]
c=copy.copy(a)
print(id(a) == id(c))
···
False
···
c[2]=5  索引不同，a和b不会同时改变，
print(a,c)
···
[1, 2, 3] [1, 22222, 3]
···


 a=[1,2,[3,4]]  #第三个值为列表[3,4],即内部元素
d=copy.copy(a) #浅拷贝a中的[3，4]内部元素的引用，非内部元素对象的本身
>>> id(a)==id(d)
False
>>> id(a[2])==id(d[2])
True
>>> a[2][0]=3333  #改变a中内部原属列表中的第一个值
>>> d             #这时d中的列表元素也会被改变
[1, 2, [3333, 4]]

#copy.deepcopy()

>>> e=copy.deepcopy(a) #e为深拷贝了a
>>> a[2][0]=333 #改变a中内部元素列表第一个的值
>>> e
[1, 2, [3333, 4]] #因为时深拷贝，这时e中内部元素[]列表的值不会因为a中的值改变而改变
>>>
