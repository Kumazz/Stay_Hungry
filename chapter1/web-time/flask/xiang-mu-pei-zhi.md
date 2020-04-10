# 项目配置
&emsp;&emsp;非 IDEA 创建的项目，默认情况下 Flask 不会开启 DEBUG 模式，开启该模式可以将代码错误显示在终端上，方便调试
* ### 设置 DEBUG 模式
&emsp;&emsp;**有三种开启模式**

```python
    from flask import Flask
    
    # 在应用对象上设置
    app.debug = True
    
    # 在 config 属性中设置
    app.config.update(DEBUG=True)
    
    app = Flask(__name__)
    @app.route('/')
    def index():
        return 'Hello Flask'
    if __name__ = '__main__':
    # 在执行 run 方法作为参数传递进去
        app.run(debug=True)

```






