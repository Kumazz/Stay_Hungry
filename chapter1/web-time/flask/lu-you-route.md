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
  # 尖括号是固定写法，通过 converter即类型名称来制定类型,variable 默认数据类型是【字符串】
  @app.route('/< converter:variable >/')
```
&emsp;&emsp; 构造整型 id 的 aticles URL，同时可以构造浮点型

```python
  @app.route('/aticles/<int:id>')
  def aticles(id):
    return f'Hello Flask 的第{id}篇'
```
&emsp;&emsp;构造携带 / 的 URL

```python
  @app.route('/aticles/<path:test>/')
  def url_path(test):
    return f'携带了 / 的路径'

```
&emsp;&emsp; 构造指定多种路径,item()可以接收两个 URL，一定要传 url_path 参数，url_path名称任取

```python
  @app.route('/<any(url1,url2):url_path>/')
  def item(url_path):
    return url_path
    
  # 例如
  @app.route('<any(blog,aticles):url>/<id>/')
  def detail(url,id):
    if url == 'blog':
      return f'这是博客第{id}章'
    else:
      return f'这是文章第{id}章'
```
&emsp;&emsp; 构造 uuid 的 URL，用于对外显示数字

```python
  @app.route('/u/<uuid:id>')
  def u(id):
    return f'uuid是{id}'
```




  
    



    


  










