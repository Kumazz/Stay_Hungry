# 异常

### 基本语法

```python
    try:                                    # 捕获异常
        可能发生错误的代码
    except:                                 # 处理异常
        如果出现异常执行的代码

```

*  捕获指定异常


```python
    try:
        可能发生错误的代码
    except 异常类型:
        如果捕获到该异常类型执行的代码
        
    ----------------------------------
    try:
        print(num)
    except NameError:
        print('有错误')
```


```python
    
        

```




