
本项目是基于[dockur/windows](https://github.com/dockur/windows)项目搭建的bitcoin v0.1版本的开发环境, 以用来学习bitcoin最初的实现和设计。搭建的开发环境是构建了一个windows XP虚拟机，在虚拟机中安装Visual C++ 6.0来编译和调试bitcoin代码。



# 项目结构
```
data                        存放虚拟机运行数据
share                       主机与虚拟机共享目录,用来双向传输文件
share/bitcoin               bitcoin v0.1源代码
share/Visual C++ 6.0.exe    Visual C++ 6.0安装文件
compose.yml                 用来启动虚拟机环境
```


# 使用方式
1. 安装Docker
2. 下载本项目到本地
3. 进入项目根目录,执行`docker compose up`启动虚拟机环境
4. 打开浏览器,访问`http://localhost:8006`，等待Windows XP安装完成
5. 在Windows XP桌面上把Shared目录中的bitcoin目录和Visual C++ 6.0.exe文件复制到桌面
6. 把`bitcoin/dll`目录中的所有文件复制到`C:\Windows\System32`目录
7. 双击`bitcoin/bin/bitcoin.exe`,启动比特币客户端，启动成功则表示运行环境搭建完毕
6. 双击Visual C++ 6.0.exe文件,安装Visual C++ 6.0
7. 打开Visual C++ 6.0,把`bitcoin/bitcoin.dsw`文件拖拽到Visual C++ 6.0窗口,打开项目
8. 点击build按钮，编译项目
9. 点击Execute Program按钮，启动比特币客户端。

如果过程中都没有问题，则表示运行环境和开发环境搭建完毕，可以进行学习了。

# 虚拟机参数
默认虚拟机参数如下:
```
系统: Windows XP
CPU: 2
内存: 1G
硬盘: 10G
语言: 英文
键盘布局: en-US
用户名: bill
密码: gates
```
这些参数都是可调整的,具体可以参考[dockur/windows](https://github.com/dockur/windows)项目的README.md文件。

但是CPU核数和内存不要调的太大，可能Windows XP系统不支持，造成无法正常运行。
