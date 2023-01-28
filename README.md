# 如何在z6巅峰版以上的小天才设备上安装第三方应用
此教程面向有基础人群

将教授您如何在z6巅峰版以上的小天才设备上安装第三方应用

首先，您需要一个adb工具包

然后解压文件“qmmi.zip”

打开adb工具包

按住shift键，右键点击文件夹内的空白位置

选择“在此打开命令提示符”

手表打开adb，重启手表，电脑用数据线连接手表。

在命令窗口输入`adb devices`，回车

如果显示了您的设备，则证明您的设备连接正常

如果显示`Error:no emulators/devices found`，请检查您的连接，或安装驱动

接下来，在命令行内输入`冻结桌面的命令`，回车

您的手表会黑屏，不要惊慌

接下来，请按照您的设备情况来选择

z7及以下：在命令行内输入`adb shell am start com.qualcomm.qti.qmmi/com.qualcomm.qti.qmmi.framework.MainActivity`，回车

z8及以上：在命令行内输入`adb shell am start com.qualcomm.qti.qmmi/com.qualcomm.qti.qmmi.framework.MainActivity`，回车

在命令行内输入`解冻桌面命令`，回车，重启，您的设备的桌面就会恢复正常

接下来，将你想要安装的安装包放到adb工具包的文件夹里面

取一个简单的名字

在命令行里输入`adb push 文件名.apk /sdcard/文件名.apk`，回车

在命令行里输入`adb shell`，回车

在命令行里输入`pm install-create`，回车

记下输出的那串数字

在命令行里输入`pm install-write 那串数字 install /sdcard/文件名.apk`，回车

在命令行里输入`pm install-commit 那串数字`，回车

安装成功
