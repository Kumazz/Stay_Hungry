# 数据类型
### 认识数据类型
&emsp;&emsp; 应对不同的业务需求，把数据分成了 7 个不同类型，使用内置函数 type() 检查数据类型，代码如下:


```python
    myName = 'tom'
    print(type(myName))
    
    # 输出 myName 的数据类型
    <class 'int'>
```


*  数值: int（整型）、float（浮点型）
*  布尔型: True（真）、False（假）
*  字符串: str
*  列表: list
*  元组: tuple
*  集合: set
*  字典: dict


### 数据类型转换
&emsp;&emsp; 在需要转换的数据前加上要转换后的数据类型即可，代码如下:


```python
   # 1. float() -- 转换成浮点型 
   num1 = 1 
   print(float(num1)) 
   print(type(float(num1)))
   
   # 2. str() -- 转换成字符串串类型 
   num2 = 10 
   print(type(str(num2)))
   
   # 3. tuple() -- 将⼀一个序列列转换成元组 
   list1 = [10, 20, 30] 
   print(tuple(list1)) 
   print(type(tuple(list1)))
   
   # 4. list() -- 将⼀一个序列列转换成列列表 
   t1 = (100, 200, 300) 
   print(list(t1)) 
   print(type(list(t1)))
   
   # 5. eval() -- 将字符串串中的数据转换成Python表达式原本类型 str1 = '10'
   str2 = '[1, 2, 3]'
   str3 = '(1000, 2000, 3000)'
   print(type(eval(str1)))
   print(type(eval(str2)))
   print(type(eval(str3))) 

```




