# 内置高阶函数
&emsp;&emsp;把函数作为参数传递，这样的函数成为高阶函数，高阶函数是函数式编程的体现
&emsp;&emsp;函数式编程大量使用函数，减少了代码的重复修改
* **内置函数**
  * abs()，数字求绝对值
  * round()，数字四舍五入
    

        
* **高阶函数体验**


```python
    def sum_num(a, b, f):                      # 形参占位
      return f(a) + f(b)            
     
    result = sum_num(-1, 2, abs)               # 将 函数名 以实参代入
    print(result)
    
    result = sum_num(-1, 2, round)             # 只需要修改传递函数就可以改变整个函数作用
    print(result)

```

* **内置高阶函数**
  *  map()
&emsp;&emsp;map(func, list)，将传入的函数变量 func 作用到 list 变量的每个元素中，并将结果组成新的列表(Py2) / 迭代器(Py3)
  
  *  reduce()








