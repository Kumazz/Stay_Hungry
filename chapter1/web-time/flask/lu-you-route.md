# URL 与 视图
### URL 与 函数的映射
```python
  # coding:utf8
  
  # 从 flask 框架中导入 FLASK 类
    from flask import Flask
  
  # 传入 __name__ 初始化一个 Flask 实例
    app = Flask(__name__)
    
  # @app.route 装饰器，映射 URL 和执行函数，如: 将根 URL 映射到了 index 函数上
    @app.route('/')
    def index():
      return ’Hello Flask'
      
  # port指定访问端口( flask 默认端口是 5000，host=0.0.0.0是可以让局域网可以访问发的网址)
    if __name__ = '__main__':
          app.run(port=9000,host='0.0.0.0')
  
```
**详解:** 一个 URL 要与执行函数进行映射，使用的 @app.route 装饰器
&emsp;&emsp; @app.route 装饰器中可以指定 URL 的规则来进行更详细的映射


```python
  # 语法如下，尖括号是固定写法，variable 默认数据类型是字符串，可以通过 converter即类型名称来制定类型
  @app.route('/< converter:variable >/')
  
  # 构造 id 的 aticles URL
  @app.route('/aticles/<id>')
  def aticles(id):
    return f'Hello Flask 的第{id}篇'

```








