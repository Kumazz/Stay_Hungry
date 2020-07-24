# 运算符
### 算数运算符
*  混合运算优先级顺序: ()高于 ** 高于 * / // % 高于 + -
  *  参与计算的有浮点数最后结果也是浮点数
  *  无论是否有浮点数参与**除法**运算结果都是浮点数
![](/assets/QQ20200724-124854@2x.png)

### 赋值运算符
![](/assets/QQ20200724-131503@2x.png)
*  切勿将赋值运算符 “=” 读作 等于号
  *  单个变量运算符，代码如下:

```python
  num = 1
  print(num)

```
  *  单个变量运算符，代码如下:
  
  ```python
    num,str1,float1 = 10,'hello',0.5
    print(num,str1,float1)
  ```
  
  *  多变量赋相同值，代码如下
  
  ```python
    a = b = 10
    print(a,b)
  ```

### 复合赋值运算符
*  由**算数运算符**与**赋值运算符**构成，先计算算术运算符将结果通过赋值运算符赋值给左边变量
![](/assets/QQ20200724-132549@2x.png)


```python
  # 经典复合赋值运算
  c = 10
  c /= 2 + 3
  print(c)
  ---------------------------
  >>> 2.0           # 结果表明该类运算，先算复合赋值运算符右边值，再来计算复合赋值运算

```

### 比较运算符
*  比较运算符又叫关系运算符，用于判断使用，结果只返回 True 或 False
![](/assets/QQ20200724-134136@2x.png)

### 逻辑运算符
![](/assets/QQ20200724-134227@2x.png)












