Python 共内置了 list、 tuple 、dict 和 set 四种基本集合，每个集合对象都能够迭代
* tuple(元组)
tup = ('python', 2.7, 64)
for i in tup:
    print(i)
    
* dictionary
dic = {}
dic['lan'] = 'python'
dic['version'] = 2.7
dic['platform'] = 64
for key in dic:
    print(key, dic[key])
    
 set  set 集合将会去除重复项   
 
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
