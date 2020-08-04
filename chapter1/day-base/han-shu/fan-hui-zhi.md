# 返回值
### 作用
&emsp;&emsp;具有独立功能的代码块，高效实现**代码重用**

### 案例

* 简单参数



```python
    def buy():
        return '糖'
        print('ok')
    goods = buy()
    print(goods)
```
&emsp;&emsp; return 负责函数返回值
&emsp;&emsp; return 退出当前函数，导致 return 下方的所有代码(函数体内部)不执行







