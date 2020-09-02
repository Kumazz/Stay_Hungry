### 魔法方法
 &emsp;&emsp;在 Python 中，\_\_xx\_\_() 的函数叫做魔法方法，指的是具有特殊功能的函数
 
*  #### \_\_init__()
用于初始化对象，比如前面案例中电饭锅长高是与生俱来的属性，可不可以在生产过程中就赋予这些属性？通过初始化对象方式可以实现
  *  \_\_init__()方法，在创建一个对象时默认被调用，不需要手动调用
  *  \_\_init__()中的 self 参数，不需要开发者传递，Python 解释器会自动把**当前的对象引用**传递过去
  
```python
    class Washer():
      def __init__(self): # 定义初始化方法，并自动传递实例对象参数 self
          self.width = 300 # 添加实例属性
          self.height = 500

    def print_info(self):
      print(f'洗衣服的宽度是:{self.width}') # 类里面调用实例属性

    haier = Washer()
    haier.print_info()
```
  
* ####带参数的\_\_init__()
用于解决一个类创建多个对象时，给不同对象设置不同的初始化属性




