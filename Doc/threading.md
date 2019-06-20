多线程 Threading 是一种让程序拥有分身效果. 能同时处理多件事情. 一般的程序只能从上到下一行行执行代码, 不过多线程 (Threading) 就能打破这种限制

本节我们来学习threading模块的一些基本操作，如获取线程数，添加线程等。首先别忘了导入模块：

import threading
获取已激活的线程数

threading.active_count()
#2
查看所有线程信息

threading.enumerate()
```[<_MainThread(MainThread, started 140736011932608)>, <Thread(SockThread, started daemon 123145376751616)>]
```
输出的结果是一个<_MainThread(...)>带多个<Thread(...)>。


查看现在正在运行的线程

threading.current_thread()
#<_MainThread(MainThread, started 140736011932608)>
添加线程，threading.Thread()接收参数target代表这个线程要完成的任务，需自行定义

def thread_job():
    print('This is a thread of %s' % threading.current_thread())

def main():
    thread = threading.Thread(target=thread_job,)   # 定义线程 
    thread.start()  # 让线程开始工作
    
if __name__ == '__main__':
    main()
    
``` python  
import threading
import time
def thread_job():
    print('T1 start\n')
    for i in range(10):
        time.sleep(0.1)
    print('T1 finish\n')

def T2_job():
    print('T2 start\n')
    print('T2 finish\n')

def main():
    added_thread = threading.Thread(target=thread_job, name='T1')
    thread2 = threading.Thread(target=T2_job, name='T2')
    added_thread.start()
    thread2.start()
    thread2.join()
    added_thread.join()

    print('all done\n')

if __name__ == '__main__':
    main()
```    
