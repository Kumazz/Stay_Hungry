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
&emsp;&emsp;一个类可以创建多个对象





