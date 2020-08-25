# 函数加强
### 递归函数
&emsp;&emsp;一个函数在内部调用自己本身
* **特性**
  * 必须是函数内部自己调用自己
  * 必须有一个明确的递归结束条件，即为递归出口


* **应用场景**
  * 快速排序
  * 遍历文件夹下面文件
  * 阶乘
  


```python
      def sum_nums(num):
        if num == 1:
        return 1
      return num + sum_nums(num-1)

      result = sum_nums(3)
      print(result)

```






### 局部变量
&emsp;&emsp;定义在**函数体内部的变量**，即只在**函数体内部生效**

```python
    def testA():
        a = 100                 # 函数体内部定义的变量
        print(a)
    testA()                      >>> 100
    print(a)                     >>> name 'a' is not defined
        

```
&emsp;&emsp; 局部变量作用: 在函数体内部，临时保存数据，即当函数调用完成后，则销毁局部变量


