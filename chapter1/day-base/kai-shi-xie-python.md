# 开始写 Python
### Hello Python
&emsp;&emsp;Python 环境主要包括: Lib( site-pakages、标准库 )、Scripts( pip.exe )、pythonexe，虚拟环境等同于 Python 环境的副本
&emsp;&emsp;区别在于 通过环境名称( venv1、venv2 )来区别环境，同时虚拟环境中没有标准库[避免复制浪费]，而Scripts包含了 pip.exe 和 python.exe
![](/assets/6A81D24BFACC32CB47B53648B67CC794.png)
### 虚拟环境工具
* ### virtualenv
&emsp;&emsp;目前最流行的 Python 虚拟环境配置工具，支持 Python2 和 Python3 并且可以为每个虚拟环境指定 Python 解释器，并选择不继承基础版本的包，缺点在于需要单独安装第三方库，无法自动记录三方依赖
* ### Pipenv
