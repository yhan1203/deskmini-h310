# 小白第一次装机且黑果记录 

## 前言

我是第一次装机且第一次装黑苹果，**我只对我自己试验过的的机型，硬件，系统镜像以及使用的efi和装机工具有发言权，其他我不懂，勿扰**。对于教程和资源下文都可以获取。鼓励大家有能力要支持正版软件，一方面，任何成果都是工程师辛苦付出的结果；再者，请大家遵守相关法律法规，**本人玩这个黑果，只是个人娱乐，如有侵犯别人版权和商业利益，请告知本人，删除相关侵权的资源和信息渠道**！！！

## 本人需求

我作为小白用户只求装完机，安安静静地使用MacOS带来的便利性，装机越简单功能越完善越好，任何软件系统重要的是服务用户的使用，我也不会不断升级，系统稳定最重要。

## 装机结果

### 完成的功能

-  Ethernet/WIFI/Bluetooth/Audio/USB&EX-USB/Sensors
-  DP/HDMI dual monitor output
-  Shutdown、Sleep
-  AppStore、ICloud、AirDrop、Handoff 
-  机箱温度变化的时候，系统对风扇能自动调速（我用的是猫扇）

### 未完成功能

1. VGA ：由于VGA基本不适用于苹果系统，就没管，因为VGA最高输出1080p分辨率的视频信号，早已经不适应时代了，而且近几年的显示器基本都有HDMI或者DP接口。

2. **重点**：很多15.4系统用户（尤其是用核显hd630的用户）都反馈，只有当睡眠唤醒的时候，主机/鼠标/键盘等其他都正常，唯独屏幕不亮，需要重新插拔一下视频线或者对屏幕重新开关机，本人就不管了，但是有这个需求的用户需要注意，听一些正版苹果用户也有反馈这个问题，因此**盲猜**是15.4系统问题。所以如果有这个可以考虑15.4之前的系统。

## 装机过程

我这个小白根据这个 [视频教程](https://www.bilibili.com/video/BV1da4y147my) ：我按照视频教程操作到 13:11，因为我的m2型号的固态硬盘上只安装MacOS，所以我只进行到 13:11，**然后不要拔掉U盘**，将U盘里面的efi（注意不是winpe目录下的efi，而是跟winpe同一级目录的efi文件夹）替换掉装完机的MacOS系统的，这一步的目的是（通俗理解）：让新装的系统开机进入系统前引导的时候，需要这个efi文件夹下的内容去欺骗MacOS，让MacOS以为目前的的硬件就是白苹果对应的硬件，这样才能正常进入MacOS系统。下一步就是：https://blog.csdn.net/weixin_43912833/article/details/102408559 。

**注意**：装机和黑果有风险，注意重要的数据提前备份。

 ## 资源

1. 目前我本人使用 efi : https://github.com/cnsilvan/deskmini310_hackintosh 大佬的分享

2. 镜像使用的是：

    -  黑果小兵分享的 [10.15.4 19E287 双EFI 分区版](https://blog.daliansky.net/macOS-Catalina-10.15.4-19E266-Release-version-with-Clover-5107-original-image-Double-EFI-Version-UEFI-and-MBR.html#more)

    - 下载镜像以后，注意校验下载的镜像有木有损坏，**必须校验**，不能跳过！

        ```
        # md5 macOS\ Catalina\ 10.15.4\(19E287\)\ Installer\ for\ Clover\ 5109\ and\ WEPE\ Support\ UEFI\ and\ MBR.dmg
        MD5 (macOS Catalina 10.15.4(19E287) Installer for Clover 5109 and WEPE Support UEFI and MBR.dmg) = c84ebeeb84c074729c11afca91c6f952
        # md5 macOS\ Catalina\ 10.15.4\(19E266\)\ Installer\ for\ Clover\ 5107\ and\ WEPE\ Support\ UEFI\ and\ MBR.dmg
        MD5 (macOS Catalina 10.15.4(19E266) Installer for Clover 5107 and WEPE Support UEFI and MBR.dmg) = e6e6e925827ee32c7e9933484cc3bb55
        ```

        