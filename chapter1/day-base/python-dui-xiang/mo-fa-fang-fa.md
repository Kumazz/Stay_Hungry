### 魔法方法
 &emsp;&emsp;在 Python 中，\_\_xx\_\_() 的函数叫做魔法方法，指的是具有特殊功能的函数
 
*  #### \_\_init__()
用于初始化对象，比如前面案例中电饭锅长高是与生俱来的属性，可不可以在生产过程中就赋予这些属性？通过初始化对象方式可以实现
  *  \_\_init__()方法，在创建一个对象时默认被调用，不需要手动调用
  *  \_\_init__()中的 self 参数，不需要开发者传递，Python 解释器会自动把**当前的对象引用**传递过去
  
```python
    class Washer():
      def __init__(self):             # 定义初始化方法，并自动传递实例对象参数 self
          self.width = 300            # 添加实例属性
          self.height = 500

    def print_info(self):
      print(f'洗衣服的宽度是:{self.width}')       # 类里面调用实例属性

    haier = Washer()
    haier.print_info()
```
  
* ####带参数的\_\_init__()
用于解决一个类创建多个对象时，通过**传递参数**给不同对象设置不同的初始化属性(上述案例中不同对象属性被固定住了)

```python
    class Washer():
        def __init__(self, width, height):
            self.width = width
            self.height = height

        def print_info(self):
            print(f'洗衣机的宽带是{self.width}')

    haier = Washer(300, 100)
    haier.print_info()

    geli = Washer(400, 200)
    geli.print_info()
      
```

* ####\_\_str__()
当使用 print 输出对象的时候，默认打印对象的内存地址。如果类定义了 \_\_str__ 方法，那么就会打印从这个方法中 return 的数据



```python
    class Washer():
        def __init__(self):
            self.width = 300

        def __str__(self):
            return '情况说明'

    haier = Washer()
    print(haier)

```

* ####\_\_del__()
当删除对象是， Python 解释器也会默认调用 \_\_del__()方法











