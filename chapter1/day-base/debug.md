# Bug与输入(出)、转义结束符
### Bug
&emsp;&emsp; bug指程序运行时出现错误，debug指调试bug纠正错误
*  常规排查方法: 通过IDE报错查看报错类型排查
![](/assets/QQ20200723-114051@2x.png)


    *  SyntaxError: 语法错误，代码不符合 Python 的语法规范 
       *  invalid character in identifier: 有无效标识符，检查一下中英文符号
       *  unexpected EOF while parsing: 无法解析的符号，检查一下是否多了或者少了括号
       
       
    *  IndexError: 索引错误，超出索引范围
       *  list index out of range: 检查列表是否正确
  
       
    *  TypeError: 数据类型错误，该数据不是正确的数据类型
       *  must be str, not int: 字符串和数字直接拼接，检查一下数据类型
       
       
    *  IndentationError: 缩进错误
       *  expected an indented block: 检查一下代码的缩进是否正确
       
       
    *  IndentationError: 缩进错误
       *  expected an indented block: 检查一下代码的缩进是否正确


    *  KeyError: 键错误
       *  "fond": 字典中没有该的key对应的值，检查一下键名或者字典数据是否正常
    
          
    *  ValueError: 值错误
       *  substring not found: 输入的数据类型跟要求的不符合
       
    *  NameError: 未初始化对象
       *  name "a" is not defined: 变量没有被定义
       
       
    *  AttributeError: 属性错误，检查一下数据类型
       * "tuple" object has no attribute "remove": 该对象没有这个属性、方法
       
    
    * UnicodeDecodeError: 编、解码错误
       * UnicodeDecodeError/UnicodeEncodeError/UnicodeTranslateError: 解码/编码/转换时的错误
       

### Debug
&emsp;&emsp; Pycharm 集成了调试程序的 Debug 工具
*  断点调试方法: 在要调试的代码第一行与代码行号位置**单击**后形成红色标注即打上断点，运行 Debug 调试，快捷键: Ctrl + Shift + D
![](/assets/QQ20200723-132551@2x.png)


### 输入与格式化输出
&emsp;&emsp; 输出: 程序输出内容给用户
&emsp;&emsp; 格式化输出: 程序输出内容给用户
&emsp;&emsp; 输入: 用户输入给计算机

*  输出，print()
   *  旧式格式符号输出，不推荐使用，但需要了解，[点击查看](https://www.jianshu.com/p/617cc100b1bf)，代码如下:
   ```python
      weight = 72.3
      id = 1
      
      # %.1f，即 % 是占位符，.1 表示保留小数位，f 表示输出是数据类型是浮点型
      print('我的体重是%.1f公斤'%weight)
      ------------------------------------------------
      >>> 我的体重是75.3公斤
      
      # 学号 001，%03d指的是 以0开头，占位3个不足以0补全
      print('我的学号是%03d'%id)
      ------------------------------------------------
      >>> 我的学号是001
      
      # print()括号内可以进行计算，多个输出用括号包裹，逗号隔开输出内容
      print('我明年%d岁了，体重还是%.1f公斤'%(age + 1,weight))
   ```
   
   *  format 格式化输出，Python3.6 之前的格式化输出写法，代码如下:
   ```python
      
   ```
   
   *  f'{表达式}' 格式化输出，Python3.6 新增写法，代码如下:
   ```python
      print(f '我的学号是{id}' )
   ```


### 转义与结束符
*  结束符: end='结束符':


```python
   print('python',end=',')
   -------------------------------
   >>> python,

```

*  常用转义符:
   *  \n: 换行
   *  \t: 制表符，一个 tab 键( 4 个空格)的距离
   
   ```python
      # print()， 默认⾃自带 end="\n" 这个换⾏结束符，代码如下:
      print('hello')
      print('python')
      ---------------------------------------
      >>> hello
      >>> python
      
      # 利用换行符进行换行，代码如下:
      print('hello\npython')
      -------------------------------------
      >>> hello
      >>> python

   ```


   










       
    
    
      
