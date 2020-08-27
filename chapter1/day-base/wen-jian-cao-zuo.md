# 文件操作

### 文件基本操作
*  **打开，open(filename,mode)**，打开一个文件，**如果没有就会自动新建文件**，有以下模式（mode）
  *  读(r)
  *  写(w)


```python
    # 基本文件操作过程
    fp = open('test.txt','w')         # 新建 test.txt 文件，并且该文件给予写入权限，赋值与一个变量
    fp.write('aaa')                   # 写入内容
    fp.close()                        # 一定要关闭文件

```


  
*  **操作**
  * 写，write()
  * 读，read()
    * readline()  
    
    
*  **关闭，close()**




