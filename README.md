# Deepin 玲珑应用 相关的常见问题及解决方案
## 1.如何安装玲珑应用
    ● 访问玲珑的官方网站[https://store.linglong.dev](https://store.linglong.dev)
    ● 单击`install`
    ● 在弹出的对话框中，选择`打开 odg-open`
    ● 等待安装完成
## 2.Deepin无法安装玲珑应用
### (1)没有安装玲珑环境
**Deepin V20**  
使用`uname -r`查看内核版本。
```
uname -r
```
输出如下：
```
5.10.101-amd64-desktop
```
内核版本要求>=4.19。  
*x86架构4.19内核需要开启user namespace。*  

使用apt安装玲珑环境：  
```
sudo apt install linglong-builder \
                 linglong-box \
                 linglong-dbus-proxy \
                 linglong-bin \
                 linglong-installer
```

**Deepin V23**  
已预装玲珑环境,无需安装。
### (2)浏览器版本太旧
从[Google Chrome](https://www.google.cn/intl/zh-CN/chrome/)官网下载最新版本的Chrome浏览器。  
![chrome](https://github.com/YuanTheta/Deepin-Linglong/raw/main/Pictures/chrome.jpg)
## 3.右键菜单中无法卸载玲珑应用
使用`ll-cli list`查看已安装的玲珑应用。
```
ll-cli list
```
复制将要卸载的应用的`appId`。

使用`ll-cli uninstall`+`appId`卸载玲珑应用。  
例如：
```
ll-cli uninstall org.deepin.calculator
```

等待卸载完成即可。

默认卸载最高版本，可以通过`appid`后附加对应版本号卸载指定版本：
例如：
```
ll-cli uninstall org.deepin.calculator/5.1.2
```
