导入线程,队列的标准模块 ¶
import threading
import time
from queue import Queue

定义一个被多线程调用的函数 
函数的参数是一个列表l和一个队列q，函数的功能是，对列表的每个元素进行平方计算，将结果保存在队列中

def job(l,q):
    for i in range (len(l)):
        l[i] = l[i]**2
    q.put(l)   #多线程调用的函数不能用return返回值
    
定义一个多线程函数 
在多线程函数中定义一个Queue，用来保存返回值，代替return，定义一个多线程列表，初始化一个多维数据列表，用来处理：
def multithreading():
    q =Queue()    #q中存放返回值，代替return的返回值
    threads = []
    data = [[1,2,3],[3,4,5],[4,4,4],[5,5,5]]    
    
import threading
from queue import Queue

def job(l, qk):
    for i in range(len(l)):
        l[i] = l[i] ** 2
    qk.put(l)

def multithreading():
    ql = Queue()  # q中存放返回值，代替return的返回值
    threads = []
    data = [[1, 2, 3], [3, 4, 5], [4, 4, 4], [5, 5, 5]]
    for i in range(4):  # 定义四个线程
        t = threading.Thread(target=job, args=(data[i], ql))  # Thread首字母要大写，被调用的job函数没有括号，只是一个索引，参数在后面
        t.start()  # 开始线程
        threads.append(t)  # 把每个线程append到线程列表中
    for thread in threads:
        thread.join()
    results = []
    for _ in range(4):
        results.append(ql.get())  # q.get()按顺序从q中拿出一个值
        print(results)
multithreading()    
