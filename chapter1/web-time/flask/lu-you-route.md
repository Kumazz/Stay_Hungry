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
&emsp;&emsp; 构造指定多种路径,item()可以接收两个 URL，一定要传 url_path 参数，url_path名称任取

```python
  @app.route('/<any(url1,url2):url_path>/')
  def item(url_path):
    return url_path
    
  # 例如
  @app.route('/<any(blog,aticle):url>/<id>/')
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
&emsp;&emsp;构造携带 / 的 URL

```python
  @app.route('/aticles/<path:test>/')
  def url_path(test):
    return f'携带了 / 的路径'

```

### URL 末尾的斜杠
&emsp;&emsp; URL 的末尾有没有斜杠是两个不同的 URL，推荐设置时末尾带斜杠

```python
  # 设置末尾带斜杠的 URL: /user/，如果访问时写成 /user，页面会自动补全后面斜杠
  @app.route('/user/')
  def user():
    return '用户中心'
    
  # 设置末尾不带斜杠的 URL: /user，访问时写成 /user/，页面会抛出 404 错误
  @app.route('/user')
  def user():
    return '用户中心'

```

### 构造 URL ( url_for )
&emsp;&emsp; url_for函数可以通过函数获取 URL，解决修改一处 URL 对应的函数名，不用导出去替换 URL，同时该函数会转义一些特殊字符和 unicode 字符串


```python
  from flask import Flask,url_for
  app = Flask(__name__)
  
  @app.route('/article/<id>/')
  def article(id):
    return f'这是文章第{id}章'
    
  @app.route('/')
  def index():
    return url_for('article',id=1)
    
```
### 指定 HTTP 方法
&emsp;&emsp; 在@app.route()中传入关键字参数 methods 来指定 HTTP 方法，默认使用 GET 请求


```python
  @app.route('/',methods=['GET','POST'])

```
### 重定向
&emsp;&emsp; 通过 flask.redirect(location,code=302)这个函数来实现重定向，默认 302 即 暂时性重定向，可以修改code=301实现永久重定向
```python
  from flask import Flask,url_for,redirect
  app = Flask(__name__)
  @app.route('/login/',methods=['GET','POST'])
  def login():
    return '注册页面'
    
  @app.route('/unname/')
  def unname():
    name = request.args.get('name')
    if not name:
      return redirect(url_for('login'))
    else:
      return name

```














  
    



    


  










