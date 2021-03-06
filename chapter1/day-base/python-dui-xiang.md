# 面向对象
### 发展过程
&emsp;&emsp;面向机器 --> 面向过程 --> 面向对象
*  **面向机器:**直接使用二进制码来表示机器能够识别和执行的指令和数据

### 定义
&emsp;&emsp;面向对象是一种**抽象化的编程思想**，很多编程语言都有的一种思想
*  **类**是对一系列**具有相同特征和行为**的事物的统称，是一个**抽象的概念**，不是真是存在的事物
  *  特征即是属性，也就是变量
  *  行为即是方法，也就是函数
  
  
* **对象**是类创建出来的真实存在的事物

&emsp;&emsp;用 电饭锅图纸 - 电饭锅 - 做饭 举例，类就是设计制作电饭锅的图纸，也就是说**类是用来创建对象**的模板，电饭锅或某品牌电饭锅是根据图纸制作出来的真实存在的事物，即**对象**，而电饭锅尺寸大小就是**属性**，电饭锅烧饭蒸菜就是**方法、功能**

  
### 定义类和调用
&emsp;&emsp;Python2 中类分为: 经典类 和 新式类，区别在于经典类参数不继承 object

```python
    class 类名(object):                  # 1. 先用 class 定义类
        代码1
        代码2
        ....
        
    对象名 = 类名(参数)              # 2. 创建对象: 将类名()赋值给变量(对象名)进行实例化
    对象名.函数()                   # 3. 调用方法

```
&emsp;&emsp; 先用** class **定义类再创建对象，** 类名() **赋值变量创建对象，类名要符合 Python 标识符命名规范，同时遵循**大驼峰命名习惯**；


```python
    class Ecooker():                        # 用 class 定义类，定义一个电饭锅这个类
        def wash(self):                     # 用 函数 定义方法，self 在 Python中解释器会自动补充
            print('能洗衣服')

    haier = Ecooker()                       # 创建对象，实例化对象，创建一个海尔电饭锅
    haier.wash()                            # 调用 势力/对象方法

```





