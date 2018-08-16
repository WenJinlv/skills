> 所有的函数其实都是可调用的对象。

当一个类实现__call__方法时， 这个类的实例就会变成可调用对象。



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