装饰器@
```python
import time
def timer(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"函数 {func.__name__} 执行时间为: {end_time - start_time} 秒")
        return result
    return wrapper
@timer
def my_function():
    # 假装这个函数执行了一些操作
    return result
```
等价于 
```python
def my_function():
    # 假装这个函数执行了一些操作
    return result
my_function = timer(my_function)
```

