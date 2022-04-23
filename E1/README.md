# 实验1——安装相关软件

链接跳转：[主目录](https://github.com/ZW-Q/MySoftware-Development-Practice)	[实验1](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E1)	[实验2](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E2)	[实验3](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E3)	[实验4](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E4)	[实验5](https://github.com/ZW-Q/MySoftware-Development-Practice/tree/main/E5)

```
实验内容
1. 安装Android Studio 4.1 之上的版本，更好的支持 TensorFlow lite。
2. 安装Jupyter Notebook和相关的Python环境，后续用于机器学习模型构建。
3. 探索两个软件的使用方法。
4. 使用Jupyter Notebook将上述安装过程以Markdown语法描述，并上传至Github。
```

------

## 一、卸载Android Studio


### 1、进入控制面板，点击卸载Android Studio

<img src="Images/Unistall Software/Control Panel Unistall Android Studio.png" style="zoom:67%;" />

### 2、进入用户目录删除.android和.gradle文件夹

```
C:\Users\qiaoqiao  <qiaoqiao>为用户名
```

<img src="Images/Unistall Software/delete .gradle and .android.png" style="zoom:67%;" />

### 3、重新启动电脑，即可卸载成功

------

## 二、安装Android Studio 2021.1.1 Patch 3并配置

### 1、去官网下载安装包

[Android Studio官网]: https://developer.android.google.cn/studio

<img src="Images/Install Software/Install Android Studio/Android Studio Web.png" style="zoom:67%;" />

### 2、安装Android Studio

#### ① 运行安装包

<img src="Images/Install Software/Install Android Studio/Android Studio1.png" style="zoom:67%;" />

#### ② 选择虚拟机

<img src="Images/Install Software/Install Android Studio/Android Studio2.png" style="zoom:67%;" />

#### ③ 修改安装路径

<img src="Images/Install Software/Install Android Studio/Android Studio3 Modify Path.png" style="zoom:67%;" />

#### ④ Android Studio IDE安装成功

<img src="Images/Install Software/Install Android Studio/Android Studio4.png" style="zoom:67%;" />

### 3、修改hosts文件

```
C:\Windows\System32\drivers\etc\hosts
```

#### ① 取消勾选只读选项

<img src="Images/Install Software/Install Android Studio/hosts1 cancel read only.png" style="zoom:67%;" />

#### ② 打开hosts文件

<img src="Images/Install Software/Install Android Studio/hosts2 open.png" style="zoom:67%;" />

#### ③ 编辑hosts文件

```
#Android 
203.208.40.33 dl.google.com
```

<img src="Images/Install Software/Install Android Studio/hosts3 update.png" style="zoom:67%;" />

### 4、安装Android SDK

#### ① 启动Android Studio

<img src="Images/Install Software/Install Android Studio/AndroidStudio.png" style="zoom:67%;" />

#### ② 修改安装路径

<img src="Images/Install Software/Install Android Studio/InstallSDK1.png" style="zoom:67%;" />

#### ③ 安装license

<img src="Images/Install Software/Install Android Studio/InstallSDK2.png" style="zoom:67%;" />

<img src="Images/Install Software/Install Android Studio/InstallSDK3.png" style="zoom:67%;" />

#### ④ 安装成功

<img src="Images/Install Software/Install Android Studio/InstallSDK4.png" style="zoom:67%;" />

### 5、新建Helloworld项目

#### ① 选择New Project

<img src="Images/Install Software/Install Android Studio/NewProject1.png" style="zoom:67%;" />

#### ② 选择Empty Activity

<img src="Images/Install Software/Install Android Studio/NewProject2.png" style="zoom:67%;" />

#### ③ 项目名，项目配置

<img src="Images/Install Software/Install Android Studio/NewProject3.png" style="zoom:67%;" />

#### ④ 构建gradle

<img src="Images/Install Software/Install Android Studio/NewProject4.png"  />

### 6、安装虚拟机

#### ① Device Manager 选择Create Device

<img src="Images/Install Software/Install Android Studio/CreateDevice1.png" style="zoom:67%;" />

#### ② 选择Pixel 2

<img src="Images/Install Software/Install Android Studio/CreateDevice2.png" style="zoom:67%;" />

#### ③ 下载API 32 

<img src="Images/Install Software/Install Android Studio/CreateDevice3.png" style="zoom:67%;" />

#### ④ 选择API 32并且下一步

<img src="Images/Install Software/Install Android Studio/CreateDevice4.png" style="zoom:67%;" />

#### ⑤ 命名AVD Name，虚拟机安装成功

<img src="Images/Install Software/Install Android Studio/CreateDevice5.png" style="zoom:67%;" />

### 7、运行Helloworld项目

#### ① 启动虚拟机

<img src="Images/Install Software/Install Android Studio/RunDevice1.png" style="zoom:67%;" />

#### ② 启动app，运行成功

<img src="Images/Install Software/Install Android Studio/RunDevice3.png" style="zoom:67%;" />

------

## 三、卸载Anaconda

### 1、安装 Anaconda-Clean package
#### ① 打开 Anaconda Prompt

<img src="Images/Unistall Software/Start Anaconda Prompt.png" style="zoom:67%;" />

#### ② 输入如下命令

```
conda install anaconda-clean
```

<img src="Images/Unistall Software/conda install anaconda-clean.png" style="zoom:67%;" />

### 2、输入如下命令卸载

```cmd
anaconda-clean
```

<img src="Images/Unistall Software/anaconda-clean.png" style="zoom:67%;" />

### 3、进入Anaconda安装目录，运行Uninstall-Anaconda3.exe
<img src="Images/Unistall Software/Uninstall Anaconda.png" style="zoom:67%;" />

#### 卸载中...

<img src="Images/Unistall Software/unistall Anaconda.png" style="zoom:67%;" />

### 4、重新启动电脑，即可卸载成功

------

## 四、安装Anaconda 3并配置

### 1、下载安装包

[Anaconda官网]: https://www.anaconda.com/products/distribution

<img src="Images/Install Software/Install Anaconda/Anaconda Web.png" style="zoom:67%;" />

### 2、安装

#### ①  运行安装包

<img src="Images/Install Software/Install Anaconda/Anaconda1.png" style="zoom:67%;" />

#### ② Accept License

<img src="Images/Install Software/Install Anaconda/Anaconda2.png" style="zoom:67%;" />

#### ③ 仅为我安装

<img src="Images/Install Software/Install Anaconda/Anaconda3 Just Me.png" style="zoom:67%;" />

#### ④ 修改安装路径

<img src="Images/Install Software/Install Anaconda/Anaconda4 Modify Path.png" style="zoom:67%;" />

#### ⑤ 注册python，取消勾选配置环境变量

<img src="Images/Install Software/Install Anaconda/Anaconda5register python.png" style="zoom:67%;" />

#### ⑥ 安装中

<img src="Images/Install Software/Install Anaconda/Anaconda6.png" style="zoom: 67%;" />

#### ⑦ 安装完成

<img src="Images/Install Software/Install Anaconda/Anaconda7.png" style="zoom:67%;" />

### 3、打开Anaconda Navigator

<img src="Images/Install Software/Install Anaconda/Anaconda Navigator.png" style="zoom:67%;" />

#### ① 打开Prompt，输入conda list

<img src="Images/Install Software/Install Anaconda/Anaconda Prompt.png" style="zoom:67%;" />

#### ② 出现如下即为成功

<img src="Images/Install Software/Install Anaconda/conda list.png" style="zoom:67%;" />

------

## 五、安装Jupyter Notebook并配置

### 1、方法1：使用pip安装Jupyter Notebook

#### ① 查看Python和pip版本

```
Python -V
pip -V
```

#### ② 升级pip到最新版本

```
pip3 install --upgrade pip
```

#### ③ 安装Jupyter Notebook

```
pip install jupyter
```

#### ④ 安装完成

<img src="Images/Install Software/Install Jupyter Notebook/pip install Juypter Notebook.png" style="zoom:67%;" />

### 2、方法2：通过Anaconda打开Jupyter Notebook

#### ① 打开Anaconda Navigator

#### ② 打开Jupyter Notebook

<img src="Images/Install Software/Install Jupyter Notebook/open Jupyter Notebook.png" style="zoom:67%;" />

#### ③ 出现如下界面即为成功

<img src="Images/Install Software/Install Jupyter Notebook/Jupyter Notebook.png" style="zoom:67%;" />

### 3、修改Jupyter Notebook默认目录

#### ① 打开Anaconda Prompt

<img src="Images/Install Software/Install Jupyter Notebook/Jupyter Modify Path1.png" style="zoom:67%;" />

#### ② 在Prompt输入命令，生成配置文件

```
jupyter notebook --generate-config
```

<img src="Images/Install Software/Install Jupyter Notebook/Jupyter Modify Path2.png" style="zoom:67%;" />

#### ③ 打开`jupyter_notebook_config.py`文件，打开后找到`#c.NotebookApp.notebook_dir = ''`这一行代码,删除行首的`#`

<img src="Images/Install Software/Install Jupyter Notebook/Jupyter Modify Path3.png" style="zoom:67%;" />

#### ④ 将 `' '`中改为所更改的路径

![](Images/Install Software/Install Jupyter Notebook/Jupyter Modify Path4.png)

#### ⑤ 再次打开Jupyter Notebook，目录已更改

<img src="Images/Install Software/Install Jupyter Notebook/Jupyter Modify Path5.png" style="zoom:67%;" />

<img src="Images/Install Software/Install Jupyter Notebook/Jupyter Modify Path6.png" style="zoom:67%;" />

#### ⑥ 新建Python3编辑文件

<img src="Images/Install Software/Install Jupyter Notebook/New Notebook1.png" style="zoom:67%;" />

<img src="Images/Install Software/Install Jupyter Notebook/New Notebook2.png" style="zoom:67%;" />