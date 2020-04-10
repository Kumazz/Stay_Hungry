# Flask

>**轻量级 Web 框架，模板、ORM等通过拓展(包)提供功能，适合学习者学习框架开发**

### 扩展包
&emsp;&emsp;**Flask-SQLAIchemy:** 操作数据库
&emsp;&emsp;**Flask-migrate:** 管理迁移数据库
&emsp;&emsp;**Flask-WTF:** 表单
&emsp;&emsp;**Flask-RESTful:** 开发 REST API 的工具
&emsp;&emsp;**Flask-script:** 插入脚本
&emsp;&emsp;**Flask-Login:** 认证用户状态
&emsp;&emsp;**Flask-Bootstrap:** 集成前端 Twitter Bootstrap 框架
&emsp;&emsp;**Flask-Mail:** 邮件
### 开发文档
&emsp;&emsp;[中文文档](https://dormousehole.readthedocs.io/en/latest/)
### Pycharm 设置
![](/assets/QQ20200410-093437@2x.png)
**注意:** 用 IDEA 创建 Flask 项目就不需要再 pip install flask，已经安装了基础扩展包
![](/assets/QQ20200410-094703@2x.png)
**注意:** 因为 Pycharm2018 版本后，直接创建 Flask需要在编辑项目中开启 debug 模式和更改端口号
### 初识 Flask

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























