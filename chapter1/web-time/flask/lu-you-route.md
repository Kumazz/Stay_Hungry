# 视图



```python
  # coding:utf8
  
  # 从 flask 框架中导入 FLASK 类
    from flask import Flask
  
  # 传入 __name__ 初始化一个 Flask 实例
    app = Flask(__name__)
    
  # app.route装饰器，映射 URL 和执行函数，如: 将 index URL 映射到了 index 函数上
    @app.route('/index/')
    def index():
      return ’Hello Flask'
      
  # port指定访问端口( flask 默认端口是 5000，host=0.0.0.0是可以让局域网可以访问发的网址)
    if __name__ = '__main__':
          app.run(port=9000,host='0.0.0.0')
  
```
**注意:** @ 左右不能有空格；ip地址指的是访问机器的地址，不写就默认是本地







