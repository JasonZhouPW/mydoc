##  使用conda管理

> conda可以直接创建不同python版本的虚拟环境。前面讲的virtualenv只是指定创建不同python版本的虚拟环境，前提是你的电脑上已经安装了不同版本的python,与conda相比没有conda灵活。

### 1. 安装

下载anaconda安装的python直接可以使用conda工具

### 2. 创建虚拟环境

创建不同的python版本，直接写出版本号就好了，还可以同时安装想要的库。

```text
# Python 2.7  
$ conda create -n venv python=2.7  

# Python 3.4  
$ conda create -n venv python=3.4  

# Python 3.5  
$ conda create -n venv python=3.5
```

### 3. 激活虚拟环境

```text
#on windows
activate venv
#on linux
source activate venv
```

### 4. 退出虚拟环境

```text
#on windows
deactivate
#on linux
source deactivate
```

### 5. 删除虚拟环境

```text
# 删除一个已有环境
conda remove --name venv --all
```

### 6. 其他有用指令

```text
# 列出系统存在虚拟环境
conda info -e
conda env list

# 查看当前环境下已安装的包
conda list

# 查看某个指定环境的已安装包
conda list -n venv

# 查找package信息
conda search numpy

# 安装package
conda install -n venv numpy
# 如果不用-n指定环境名称，则被安装在当前激活环境
# 也可以通过-c指定通过某个channel安装

# 更新package
conda update -n venv numpy

# 删除package
conda remove -n venv numpy
```

