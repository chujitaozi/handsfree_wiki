# 如何配置环境
本节介绍如何在Ubuntu 14.04上安装ros并配置HandsFree程序

# 安装ROS
HandsFree支持ROS的indigo版本和Kinetic，在14.04上只支持indigo，可以参考[官方安装教程](http://wiki.ros.org/indigo/Installation/Ubuntu)，也可以下载我们的脚本进行安装：
```
cd ~
wget https://raw.githubusercontent.com/chujitaozi/Scripts/master/ros/indigo_install.sh
sh indigo_install.sh
```
其中可能需要管理员密码，安装结束后，关闭终端。  
测试一下，在终端中运行：
>roscore

和
>rosrun turtlesim turtlesim_node

如果出现了小乌龟，说明安装成功啦。

<div align=center><img src="/images/FAQ/environment_config/turtlesim.png"/></div>

# 配置HandsFree环境
HandsFree 可以按照github上的README进行安装，也可以直接通过下面的脚本进行安装：
```
cd ~
wget https://raw.githubusercontent.com/chujitaozi/Scripts/master/ros/install.sh
sh install.sh
```
默认安装路径为/opt/ros_handsfree/src   
安装成功后可以使用USB连接到主控板侧面的Micro USB插口，然后执行：
>roslaunch handsfree_hw handsfree_hw.launch

![handsfree_hw_node](/images/Tutorial/7/7.1/1_hf_robot_node.png)
如果如上图显示，则说明连接成功，如果出现timeout，请参考[常见问题](/doc/....)
