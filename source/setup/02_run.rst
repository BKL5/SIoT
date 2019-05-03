安装运行
=========================

SIoT是一个绿色软件，将下载的压缩包解压并打开后，你能看到多个文件，如：

| SIoT_win.exe（Win10版本执行文件）
| SIoT_mac（Mac版本可执行文件）
| SIoT_linux（Linux版本执行文件）

注：更多操作系统支持的文件在不断增加中。我们正在开发windows下的“启动助手”，让软件的使用更加方便。

根据自己的操作系统，你可以运行相对应的软件。

Window版本：
-----------

双击运行SIoT_win.exe，将看到一个黑色的CMD窗口，如果你想维持你的计算机作为MQTT服务器的话，请不要关闭它。

Mac版本：
------------

打开终端运行，转到相应目录然后执行命令，如“./SIoT_mac”。

注意：直接双击运行会出现错误！程序没有读取配置文件的权限问题，将默认开启的是8082端口。

如果担心程序被删除，可以使用nohup命令。

参考命令：nohup node /Users/xiezuoru/Desktop/iot_test/SIOT_Mac &
其中“/Users/xiezuoru/Desktop/iot_test/SIOT_Mac”为程序的路径。

linux版本：
-----------

nohup ./SIoT_linux &
其中“SIoT_linux”为程序的路径。


服务器信息
---------
SIoT启动后，你的计算机（电脑）就成为了一个标准的MQTT服务器：
服务器地址：计算机（电脑）局域网IP地址
MQTT端口：1883
用户名：siot（小写）
默认密码：dfrobot（小写）
消息主题（Topic）：项目名/设备名（可以自定义）
Web管理地址：电脑IP:8080

注：可以通过config.json文件修改用户名、密码和端口等信息。

