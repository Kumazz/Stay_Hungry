# 数据类型
### 值和类型
* 值，值是程序操作的**对象**之一，是**数据**的基本组成单元，比如一个字母或者数字

* 类型，对值的一种划分，应对不同的业务需求
  * Python 把值( 数据 )分成了 7 个不同类型
  * 使用内置函数 **「 type() 」** 检查数据类型


```python
    myName = 'tom'
    print(type(myName))
    -----------------------
    >>> <class 'int'>
```
    
&emsp;&emsp;&emsp;上述代码中 「 class 」这个字样表明这是一类( 型 )
* Python 中主要类型如下:
  *  数值: int（整型）、float（浮点型）
  *  布尔型: True（真）、False（假）
  *  字符串: str
  *  列表: list
  *  元组: tuple
  *  集合: set
  *  字典: dict



### 公共操作
*  运算符
![](/assets/QQ20200802-154648@2x.png)

*  方法
![](/assets/QQ20200802-155150@2x.png)
  * range()生成的序列默认从 0 开始，步长默认为 1，不包含 end 数字，返回 range 可迭代对象
  * enumerate(可遍历对象,start=0)，返回的是**元组**，元组第一个数据是原迭代对象数据的**下标**，第二个数据是原迭代对象的**数据**
  

* 数据类型转换，在需要转换的数据前加上要转换函数即可，代码如下:

  * float()转换成浮点数，**字符串**转换时中不可以包含非数字字符，**空字符串、字母都不可以转换为浮点数**
  
```python
    num1 = 1 
    print(float(num1))  
    print(type(float(num1)))
```

  * str()转换成字符串串类型

``` python 
    num2 = 10 
    print(type(str(num2)))
``` 

  *  tuple() -- 将⼀一个序列列转换成元组 


```python
    list1 = [10, 20, 30] 
    print(tuple(list1)) 
    print(type(tuple(list1)))
```


  *  list() -- 将⼀一个序列列转换成列列表 
  
```python
    t1 = (100, 200, 300) 
    print(list(t1)) 
    print(type(list(t1)))
```  

  *  eval() -- 将字符串串中的数据转换成Python表达式原本类型 

```python
    str1 = '10'
    str2 = '[1, 2, 3]'
    str3 = '(1000, 2000, 3000)'
    print(type(eval(str1)))
    print(type(eval(str2)))
    print(type(eval(str3))) 

```







