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







