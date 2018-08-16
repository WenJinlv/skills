当一个类实现__call__方法时， 这个类的实例就会变成可调用对象。

```
    class A(object):
        def __call__(self):
            print("__call__ is called.")
    
    a = A()
    a()   # a() <==> a.__call__()

    
```
有点类似c++中的函数对象, operator()()