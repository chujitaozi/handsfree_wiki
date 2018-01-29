# 概述
本节简单介绍HandsFree机器人架构。HandsFree机器人的架构主要是三个部分：硬件+嵌入式+软件。

## 硬件
硬件设备主要包括以下几部分：

* 结构部分：底盘（电机轮子各种）、云台（包括支撑架）等
* 传感器部分：激光雷达、摄像头等
* 底层电路部分：[主控（STM32系列单片机）](docs/Hardware/Control-Unit.md)、[电机驱动](docs/Hardware/Module.md)等
* 上位机：机器人端工控机（或PC）、远程PC等

## 嵌入式OpenRE

[OpenRE](docs/OpenRE/README.md)全称Open Source Robot Embedded Library ， 是一个专门为机器人写的、基于STM32系列微处理器的嵌入式开源库。   
将使用OpenRE编写机器人底层驱动程序下载到单片机主控里面，可以使主控板接受机器人PC端软件部分传来的串口数据，然后进行电机等各种关节的控制。

## 软件

软件部分运行在机器人端工控机（或PC）和远程PC上。HandsFree系列机器人使用的是基于Ubuntu操作系统的软件[ROS](http://www.ros.org/)（Robot Operating System）。Ubuntu操作系统是类似于windows系统一样运行在电脑或者ARM板上面的操作系统；ROS是运行在Ubuntu操作系统上的一个应用。你可以在这个应用里编程，很方便地实现机器人的控制、物体识别、语音识别等。更多的时候，我们把ROS称为一个次级操作系统，即机器人操作系统。    
我们提供了基于ROS的很多[教程与指导](docs/Tutorial/README.md)，从建图到导航，还有很多关于计算机视觉的实验。   
