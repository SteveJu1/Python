什么是id？一个对象的id值在Python解释器里就代表它在内存中的`地址`
copy shadow copy 和 deep copy
a=[1,2,3]
b=a 
id(a)==id(b) 索引相同，改变a或b的值，另一方同时改变
# shadow copy
import copy
c=copy.copy(a)
c[2]=5  索引不同，a和b不会同时改变，

