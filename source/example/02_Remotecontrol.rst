远程控制
=========================

今天我们将分享给大家如何利用物联网平台进行远程控制，发送指令后接收方进行相应的反应。我们利用SIoT平台远程控制掌控板灯泡的发光情况。

准备工作
-----------------

在Mind+ V1.5.3的物联网模块——MQTT中，可以通过添加扩展掌控后提供的WIFI模块，与物联网平台连接，从而实现掌控板与web端、app端的互联。用户可以根据实际需要选择阿里云、Easy IoT、OneNet和SIoT四个平台物联网平台。我们在这里以web端控制掌控板灯泡的灯光为例，简单介绍如何使用SIoT平台来远程控制掌控板的操作。
    
（一）硬件准备

掌控板及其连接线

.. image:: ../image/haoqing/Mind+yuancheng-01.png

（二）软件准备

1.搭建SIoT服务器

直接双击点击与系统匹配的SIoT运行文件，屏幕会弹出一个黑色的CMD窗口，在配置中请不要关闭它。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

2.登录SIoT平台

打开浏览器，输入url：http://localhost:8082。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

3.打开Mind+ V1.5.3编写程序

.. image:: ../image/haoqing/Mind+yuancheng-01.png

步骤
------------------
打开Mind+后，在“上传模式”下，在“扩展”中选择“主控板-掌控板”与“网络服务-WiFi、MQTT”进行安装。
 
将掌控板通过数据线连接到电脑，驱动安装完成后，点击“连接设备”中“COMxx-CP210x”即可。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

（一）参考程序

.. image:: ../image/haoqing/Mind+yuancheng-01.png

1.其中WiFi连接的热点名与密码需要手动修改成可以连接的热点信息。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

2.设置MQTT初始化参数。选择SIoT物联网平台，服务器地址为本地IP地址，账号密码即SIoT使用的账号密码，Topic_0为“项目ID/名称”。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

3.当MQTT接收到on时，全部灯泡亮白光；当MQTT接收到off时，全部灯泡亮红光。接收信息内容可以进行修改。

4.将程序“上传到设备”进行测试。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

（二）运行结果

掌控板屏幕上显示以下内容。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

SIoT平台设备每间隔10秒接受一条信息。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

在SIoT平台给掌控板发送消息“on”。掌控板的小灯全部变成了白色灯。相同操作，发送消息“off”，灯泡变色。测试成功。

.. image:: ../image/haoqing/Mind+yuancheng-01.png

参考代码
----------------

代码下载地址：
