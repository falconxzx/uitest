# 向导
 - uiautomator2介绍
 - Linux & Windows安装
 - 测试框架设计与用例编写
 
# uiautomator2介绍
项目地址：[uiautomator2][1]
## 支持平台及语言 ##
python-uiautomator2封装了谷歌自带的uiautomator2测试框架，提供便利的python接口。他允许测试人员直接在PC上编写Python的测试代码，操作手机应用，完成自动化，大大提高了自动化代码编写的效率。
## 工作原理 ##
```graphLR
    A[python-uiautomator2] -->|HTTP| B(atx-agent)
    B --> C(uiautomator.apk)
```
 - 手机连接到电脑，电脑使用adb向手机推送了一个二进制文件 atx-agent，启动atx-agent。
 - atx-agent是一个http服务器，运行在电脑上的python程序使用HTTP协议跟手机上atx-agent通信。
 - atx-agent随后启动uiautomator.apk这个应用，将收到的请求转换成UiAutomator的UI自动化操作。

## uiautomator ##
自动化驱动框架有

 - Android：UIAUTOMATOR2、UIAUTOMATOR、INSTRUMENTATION
 - iOS：UIAUTOMATAION、XCUITESTING（WebDriverAgent）

由于上面手机自动化驱动框架是由 Google （或 Apple）官方提供的，是跟 Android SDK 捆绑发布的，所以每次 Android 新的系统（SDK 升级）发布的时候，与 SDK 捆绑的自动化框架也会有升级（要么是对原有框架的优化如 Android 的 UIAUTOMATION 框架， 要么就是推出新的框架如 iOS废弃 UIAUTOMATION 框架 推出 XCUITESTING）

Android 的自动化框架 UIAutomator ，UIAutomator 框架提供了3个非常重要的类：

 - 对系统硬件按钮、坐标等操作的 Device 类（对android系统硬件按钮、坐标等进行点击、滑动如 menu 键、home 键、拖动）；
 - 定位元素控件的 UIObject 类；
 - 进阶操作的 UIScrollable 类。

## 快速入门 ##
 [uiautomator2快速入门][2]
 
----------




  [1]: https://github.com/openatx/uiautomator2
  [2]: https://github.com/openatx/uiautomator2/blob/master/QUICK_REFERENCE.md
