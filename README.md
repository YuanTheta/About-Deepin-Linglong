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

使用apt安装玲珑环境  
```
sudo apt install linglong-builder \
                 linglong-box \
                 linglong-dbus-proxy \
                 linglong-bin \
                 linglong-installer
```

**Deepin V23**  
已预装玲珑环境
### (2)浏览器版本太旧
从[Google Chrome](https://www.google.cn/intl/zh-CN/chrome/)官网下载最新版本的Chrome浏览器。  
![chrome](https://github.com/YuanTheta/Deepin-Linglong/raw/master/Pictures/chrome.jpg)
