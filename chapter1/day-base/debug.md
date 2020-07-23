# Debug
### 认识bug
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
       
    
    
      
