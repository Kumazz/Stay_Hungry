# 视图



```python
  # coding:utf8
  
  # 从 flask 框架中导入 FLASK 类
    from flask import Flask
  
  # 传入 __name__ 初始化一个 Flask 实例
    app = Flask(__name__)
    
  # app.route装饰器，映射 URL 和执行函数，如: 将根 URL 映射到了 index 函数上
    @app.route('/')
    def index():
      return ’Hello Flask'
      
  # port指定访问端口( flask 默认端口是 5000，host=0.0.0.0是可以让局域网可以访问发的网址)
    if __name__ = '__main__':
          app.run(port=9000,host='0.0.0.0')
  
```
**注意:** app.run 只适合开发，生产环境使用 UWSGI 或 Gunicorn 来启动






