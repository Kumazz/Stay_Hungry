# 项目配置
&emsp;&emsp;非 IDEA 创建的项目，默认情况下 Flask 不会开启 DEBUG 模式，开启该模式可以将代码错误显示在终端上，方便调试
* ### 设置 DEBUG 模式
&emsp;**有三种开启模式，开启成功会在终端显示相关信息( 模式状态、PIN码 )**

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
![](/assets/QQ20200410-104031@2x.png)
**注意:** DEBUG 模式会有安全隐患，只适合在开发环境下开启，因为程序有异常 DEBUG 模式下会显示错误堆栈模式方便调试同时，攻击者同样能通过显示异常信息获取攻击线索
* ### Pycharm 开启 DEBUG 模式
![](/assets/QQ20200410-094703@2x.png)
**注意:** 因为 Pycharm2018 版本后，直接创建 Flask需要在编辑项目中开启 debug 模式和更改端口号












