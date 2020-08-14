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
### 虚拟环境 Virtualenv
&emsp;&emsp;**官方解释:** 虚拟环境是 Python 解释器的副本，在虚拟环境中可以避免安装包的混乱和版本的冲突，为每个程序单独创建的虚拟环境可以保证程序只能访问虚拟环境中的包，从而保证全局解释器的整洁。
&emsp;&emsp;**通俗理解:** 虚拟环境相当于一个空间，在该空间安装的任何软件包不会影响到其他空间。实际场景: 同一台服务器旧项目是用flask 1.0 开发的新项目用的是 flask 2.0 开发，通过创建虚拟环境能进行单独配套环境开发不会相互影响


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
      
  # 运行程序
    if __name__ = '__main__':
          app.run()
  
```
**注意:** app.run 只适合开发，生产环境使用 UWSGI 或 Gunicorn 来启动























