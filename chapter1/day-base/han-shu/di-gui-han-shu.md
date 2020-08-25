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

![](/assets/WX20200825-160040@2x.png)




### 匿名函数
&emsp;&emsp;**变量名 = lambda [参数1,参数2..] ：逻辑表达式**
*  在定义函数的时候，不想给函数起一个名字。这个时候就可以用lambda来定义一个匿名函数
  *  参数：可选，通常以逗号分隔的变量表达式形式，也就是位置参数
  *  表达式：不能包含循环、return，可以包含 if...else...

```python
    def testA():
        a = 100                 # 函数体内部定义的变量
        print(a)
    testA()                      >>> 100
    print(a)                     >>> name 'a' is not defined
        

```
&emsp;&emsp; 局部变量作用: 在函数体内部，临时保存数据，即当函数调用完成后，则销毁局部变量


