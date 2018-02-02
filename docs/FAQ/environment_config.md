# 如何配置环境
本节介绍如何在Ubuntu 14.04上安装ros并配置HandsFree程序   
直达车：  

* [安装ROS](/docs/FAQ/environment_config.html#安装ros)
* [配置HandsFree环境](/docs/FAQ/environment_config.html#配置handsfree环境)
* [配置Kinect](/docs/FAQ/environment_config.html#配置kinect-1)

# 安装ROS
HandsFree支持ROS的indigo版本和Kinetic，**ubuntu14.04上只支持indigo，ubuntu16.04上只支持kinetic**，可以参考[ROS indigo官方安装教程](http://wiki.ros.org/indigo/Installation/Ubuntu)，也可以下载我们的脚本进行安装：
```
cd ~
wget https://raw.githubusercontent.com/chujitaozi/Scripts/master/ros/indigo_install.sh
sh indigo_install.sh
```
其中可能需要管理员密码，安装结束后，关闭终端。
测试一下，在终端中分别运行：
```
roscore
```

和
```
rosrun turtlesim turtlesim_node
```

如果出现了小乌龟，说明安装成功啦。

<div align=center><img src="/images/FAQ/environment_config/turtlesim.png"/></div>

# 配置HandsFree环境
HandsFree 可以按照github上的README进行安装，也可以直接通过下面的脚本进行安装：
```
cd ~
wget https://raw.githubusercontent.com/chujitaozi/Scripts/master/ros/install.sh
sh install.sh
```

默认安装路径为~/ros_handsfree/src   
安装成功后可以使用USB连接到机器人，然后执行：
```
roslaunch handsfree_hw handsfree_hw.launch
```
如果一切正常，会显示：
```
auto-starting new master
process[master]: started with pid [9562]
ROS_MASTER_URI=http://Robot:11311

setting /run_id to ffa41cce-05bd-11e8-8df0-001e64f02337
process[rosout-1]: started with pid [9575]
started core service [/rosout]
process[handsfree_hw_node-2]: started with pid [9585]
process[mobile_base/controller_spawner-3]: started with pid [9589]
process[robot_state_publisher-4]: started with pid [9591]
[ERROR] [1517317423.863958024]: hf link initialized failed, please check the hardware
[INFO] [WallTime: 1517317424.295263] Controller Spawner: Waiting for service controller_manager/load_controller
[INFO] [WallTime: 1517317424.298319] Controller Spawner: Waiting for service controller_manager/switch_controller
[INFO] [WallTime: 1517317424.301498] Controller Spawner: Waiting for service controller_manager/unload_controller
[INFO] [WallTime: 1517317424.304670] Loading controller: joint_state_controller
[INFO] [WallTime: 1517317424.351596] Loading controller: servo1_position_controller
[INFO] [WallTime: 1517317424.399306] Loading controller: servo2_position_controller
[INFO] [WallTime: 1517317424.419282] Loading controller: mobile_base_controller
[INFO] [WallTime: 1517317424.469234] Controller Spawner: Loaded controllers: joint_state_controller, servo1_position_controller, servo2_position_controller, mobile_base_controller
[INFO] [WallTime: 1517317424.479183] Started controllers: joint_state_controller, servo1_position_controller, servo2_position_controller, mobile_base_controller

```

如果如上图显示，则说明连接成功，如果出现err或timeout，请参考[常见问题](/docs/FAQ/solution-of-handsfree-hw-error.html)

# 配置Kinect 1
mini机器人使用的摄像头是Kinect 1代，本小节介绍如何配置Kinect 1。






