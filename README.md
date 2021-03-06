# Car-eye-CMS

Car-eye-cms 一个功能强大的流媒体管理平台,负责设备管理，通信，负责服务器运营，数据管理。

## Car-eye-CMS 访问地址

访问地址是:http://www.liveoss.com

为什么我们要有Car-eye-CMS？
我们已经了car-eye-server 他是基于车辆管理系统专门定制的管理平台. 而Car-eye-cms 是通用的流媒体设备，流媒体内容管理平台。


# 操作指南


## 用户登陆

输入用户名和密码，顶级登陆系统就可以登陆到car-eye-CMS系统。       

![](https://github.com/Car-eye-team/Car-eye-CMS/blob/master/login.png)  



## 基础设置

选择系统权限->参数设置->服务器参数设置

说明:

协议类型：支持RTSP, RTMP两种协议

IP：RTSP 流媒体服务器IP地址，只有类型是RTSP才有效、

端口: RTSP 流媒体服务器IP地址，只有类型是RTSP才有效

用户名: 暂时没用写 admin

密码：暂时没用写  admin

流媒体IP：RTMP服务器IP,只有类型是RTMP才有效

流媒体端口: RTMP服务器端口,只有类型是RTMP才有效

提供类型：当协议为RTSP时，需要硬件加速时候选1，否则填写0

按比例显示：填写0

缓存：当协议为RTSP的时候需要填写，建议为3，数字越小缓冲越小

是否显示码率信息：用来调试用



## 查看设备，查看位置和视频

选中设备即可看到自己设备在地图上显示出来

![](https://github.com/Car-eye-team/Car-eye-CMS/blob/master/position.png)  

选择车辆监控进入视频监控界面,当协议类型是RTSP的时候,画面如下：

![](https://github.com/Car-eye-team/Car-eye-CMS/blob/master/main.png)  

左边主要显示区域为四路标准监控的画面，有设备号，点击预览就可以远程链接设备进行视频预览。需要注意的是，这个需要与设备之间进行远程通信，建议使用car-eye-device进行视频预览。当打开设备进行预览的时候

RTSP 播放的地址格式为RTSP://ip:port/设备号?channel=通道号.sdp

其中IP为服务器流媒体的ip，端口号为流媒体的端口号，设备号请与设备端的设备编号保持一致，通道号为1-4，四个通道。

在监控画面出来后，可以通过其他播放器，如car-eye-player 或者VLC进行远程播放

 

## 查看历史记录
注：这个必须要用跟car-eye-device配合使用,具体按照car-eye通信协议实现对历史记录回放的调取工作。 
选择好设备和通道，需要回放的时间后点击视频搜索回放面就写出了视频播放文件列表

![](https://github.com/Car-eye-team/Car-eye-CMS/blob/master/channel.png) 


选择好文件后点击回放

就可以在左侧的相应通道内播放视频文件了。

 
## RTMP 模式下视频直播

该模式下，操作方式跟RTSP一样，支持暂时不支持RTMP 回放视频文件，而只支持直播服务。

当然用户也用户可以使用car-pusher工具直接将某个设备的音视频流推送到流媒体服务器，如设备号13510671870的设备，流媒体服务器120.76.235.109 端口为10085的设置下，推送上服务器。进入到主界面直接点击视频播放：

输入设备号，点击视频播放按钮，在点击flash控件就可以进行对设备的视频直播服务：

![](https://github.com/Car-eye-team/Car-eye-CMS/blob/master/rtmp.png) 


# 外部接口


# 联系我们

car-eye 开源官方网址：www.car-eye.cn    

car-eye 流媒体平台网址：www.liveoss.com  

car-eye 技术官方邮箱: support@car-eye.cn

car-eye技术交流QQ群: 590411159        

![](https://github.com/Car-eye-team/Car-eye-server/blob/master/car-server/doc/QQ.jpg)  


CopyRight©  car-eye 开源团队 2018
