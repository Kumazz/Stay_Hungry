# 拆包与引用
### 拆包
*  **组包**，将多个值同时赋给一个变量时,解释器会进行自动组包操作
*  **拆包**，是将一个序列类型的数据拆开同时赋值多个变量,解释器会进行拆包操作
  *  **元组拆包**
  
  ```python
    def return_num():
    return 120, 220

    num1, num2 = return_num()
    print(num1)                           >>> 120
    print(num2)                           >>> 220
  ```
  
  * **字典拆包**
  
  ```python
    dict1 = {'name':'tom', 'age':19}
    a, b = dict                             # 字典内是两个键值对，需要两个变量接收数据
    
    print(a)                                >>> name         # 取出的是key
    print(b)                                >>> age
    
    print(dict1[a])
  ```

*  **交换变量值**


```python
    a = 10
    b = 20
    
    a, b = b, a

```


### 引用
  * **位置参数**，函数调用时的数量，位置，参数类型必须和定义时的一致
  * **关键字参数**，使用形参的名字=输入的参数值，此时位置可与定义时不一致
  * **默认参数**，函数定义时，为参数设置一个默认值，当函数调用时，没有传入这个参数值，直接使用这个默认值
  * **可变参数**，可变参数有两种形式：一种是 \*args,另一种是 \**kwargs

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\*args：这种形式表示接受任意多个实际参数将其放到一个元组中。

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;\**kwargs：这种形式表示接受任意多个实际参数将其放到一个字典中，类似关键字参数

### 类型

