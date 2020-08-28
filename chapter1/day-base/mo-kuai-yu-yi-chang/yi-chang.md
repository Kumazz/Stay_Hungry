# 异常

### 基本语法

```python
    try:                                    # 尝试执行
        可能发生错误的代码                     # 一般 try 下方只放一行尝试执行的代码
    except:                                 # 捕获异常
        如果出现异常执行的代码                  # 处理异常

```

*  捕获指定异常


```python
    # 捕获单个指定异常 
    try:
        可能发生错误的代码
    except 异常类型:                           # 尝试执行的代码异常类型与捕获的异常类型不一致则无法捕获异常
        如果捕获到该异常类型执行的代码
        
    --------------------------------------------------------------
    try:
        print(num)
    except NameError:
        print('有错误')
```


```python
    # 捕获多个指定异常 
    try:
        print(1/0)
    except (NameError,ZeroDivisionError):             # 用元组形式加入多个异常类型
        print('有错误')

        

```


*  捕获所有异常，需要添加 Exception 这个所有程序异常的父类


```
    try:
        print(1/0)
    except Exception as e:
        print(e)
```












*  捕获异常描述信息，用于展示错误原因


```python
    try:
        print(1/0)
    except (NameError,ZeroDivisionError) as result:
        print(result)

```
*  捕获所有异常










