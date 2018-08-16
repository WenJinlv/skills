> 所有的函数其实都是可调用的对象。

一个类的实例也可以变成一个可调用对象，只需要这个类实现了\_\_call\_\_()方法。



```
    class A(object):
        def __call__(self):
            print("__call__ is called.")
    
    a = A()
    a()   # a() <==> a.__call__()

    
```
***
有点类似c++中的函数对象, operator()()
***

```
    class MetaSingleton(type):
        _instances = {}
        def __call__(cls, *args, **kwargs):
            if cls not in cls._instances:
                cls._instances[cls] = super(MetaSingleton, cls).__call__(*args, **kwargs)
            return cls._instances[cls]
    
    class Logger(metaclass=MetaSingleton):
        pass
    
    logger1 = Logger()
    logger2 = Logger()
    print(logger1, logger2)
    
```