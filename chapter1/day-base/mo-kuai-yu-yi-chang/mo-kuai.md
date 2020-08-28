# 模块
&emsp;&emsp;Python 模块是一个 Python 文件，以 .py 结尾，包含了 Python 对象定义和 Python 语句
&emsp;&emsp;模块能定义函数、类和变量，模块里也能包含可执行的代码

### 导入方式
*  **import**


```python
    # 导入模块
    import 模块名
    import 模块名1,模块名2...                 # PEP8 不推荐该写法
    
    # 调用功能
    模块名.功能名()
    --------------------------------------------------------
    import math
    print(math.sqrt(9))

```

*  **from..import..**


```python
    from 模块名 import 功能1，功能2...
    -------------------------------------------------------
    from math import sqrt
    print(sqrt(9))

```

*  **from..import ***，不建议使用



```python
    from 模块名 import *        # * 表示所有功能
    ------------------------------------------------------
    from math import *
    print(sqrt(9))

```

### 定义别名 - as
*  模块定义别名


```python
    import 模块名 as 别名

```

*  功能定义别名



```python
    from 模块名 import 功能 as 别名

```


### 制作模块












