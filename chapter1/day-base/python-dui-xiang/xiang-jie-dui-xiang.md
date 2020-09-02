### 详解对象
#### self
&emsp;&emsp;self 指的是**调用该函数的对象**


```python
    def Student():
        def info_print(self):                 # self 指的 stundent 这个对象
            print('test')
    student = Student()
    student.info_print()

```

#### 创建多个对象
&emsp;&emsp;一个类可以创建多个对象，不同对象的内存地址不一样



```python
    class Washer():
        def wash(self):
            print('洗衣服')
            print(self)

    haier1 = Washer()
    haier1.wash()
    print(haier1)                      # haier1 的内存地址与 haier2 的内存地址不一样

    haier2 = Washer()
    haier2.wash()
    print(haier2)

```

#### 属性
&emsp;&emsp;属性即特征，比如: 电饭锅的宽度、高度、重量等
&emsp;&emsp;对象属性既可以在类外面添加和获取，也能在类里面添加和获取

*  **添加属性**


```python
    对象名.属性名 = 值
    ------------------------------
    # 在类的外面添加属性
    class Washer():
        def wash(self):
            print('洗衣服')
            print(self)

        haier1 = Washer()

        haier1.width = 400                       # 类的外面添加属性
        haier1.height = 500

```



*  **获取属性**


```python
    对象名.属性名
    --------------------------------------------
    print(f'洗衣机的高度是:{haier1.height}')
```








