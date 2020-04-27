# 虚拟环境
&emsp;&emsp;Python 环境主要包括: Lib( site-pakages、标准库 )、Scripts( pip.exe )、pythonexe，虚拟环境等同于 Python 环境的副本
&emsp;&emsp;区别在于 通过环境名称( venv1、venv2 )来区别环境，同时虚拟环境中没有标准库[避免复制浪费]，而Scripts包含了 pip.exe 和 python.exe
![](/assets/6A81D24BFACC32CB47B53648B67CC794.png)
### 虚拟环境工具
* ### virtualenv
&emsp;&emsp;目前最流行的 Python 虚拟环境配置工具，支持 Python2 和 Python3 并且可以为每个虚拟环境指定 Python 解释器，并选择不继承基础版本的包
* ### Pipenv
&emsp;&emsp;基于项目的虚拟环境管理


```python
    pip install pipenv                # 安装 pipenv
    pipenv --version                  # 查看版本
    
    pipenv --python3                  # 初始化
    pipenv install flask              # 在虚拟环境下安装包，会生成Pipfile
    pipenv shell                      # 进入执行目录
    pipenv --vene                     # 查看绑定的虚拟环境
    pipenv graph                      # 查看依赖包
    exit                              # 退出
    
    pipenv install --dev [Packgename]  # 开发使用

```


* ### virtualenvwrapper
&emsp;&emsp;集中式虚拟环境管理，封装 virtualenv 便于管理，不支持 windows ，有 virtualenvwrapper-win 针对 win 平台使用
* ### venv
&emsp;&emsp;从 Python3.3 开始自带虚拟环境 venv ，不支持 Python2
* ### pyenv
&emsp;&emsp;不同版本 Python 可以在系统上共存
&emsp;**一般使用 virtualenv ，如果确定了项目没有 Python2 ，推荐使用 pipenv**
### 安装 virtualenv
* ### windows 环境


```python
    python -m venv venvdemo          # 创建 venvdemo 的虚拟环境
    cd venvedemo/Scripts             # 进入执行目录
    activate                         # 激活虚拟环境
    deactivate                       # 退出虚拟环境
```

![](/assets/C29F50964F1E757B3AC2CFA4D57D2580.png)

* ### linux 环境


```bash
    
```
### 保存复制虚拟环境


```python
    pip freeze > requirments.txt      # 保存虚拟机环境( 当前目录 )
    pip install -r requirments.text   # 复制虚拟环境

```














