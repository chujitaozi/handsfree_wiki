本节介绍Stone机器人的相关参数及Demo.

# Stone机器人

<div align=center><img src="/images/Mechanical/stone/wiki/stone_small_render.jpg"/></div>

## 概述
Stone是一款采用前万向后双驱动轮底盘布局的智能车平台。其整机结构采用平板桁架式透明化设计，外形简单又不失机械美感。Stone可搭载Dobot1、Dobot m1等小型机械臂，能支持多种激光雷达，TX1、TK1、树莓派等主流控制器。其配备高度可调的两轴云台，兼容多款RGBD摄像头和单、双目摄像头。

## 外形及性能参数

机器人参数| 值
------------ | -------------
净重(kg) | 8
整体尺寸(mm) | 400x1080
负载(kg) | 15
最大速度(m/s) | 1.2
电池容量(mAh) | 12V 16000
续航时间(h) | 12
充电时间(h) | 5
驱动方式 | 两轮差分驱动
电源扩展 | 19V/3A x 3 ,  12V/10A x 5 , 12V/3A x 4 , USB5V/2A x 2 , 一路急停12V/10A
电机控制接口数量 | 4
内部传感器 | 集成编码器 , 陀螺仪 , 磁力计 , 气压计 , 可扩展超声/红外传感器 
通信扩展接口 | USB-USART x 1 , USART x 2, Bluetooth x 1 , CAN x 1 , SPI x 1 
支持安装的设备 | RplidarA1/A2，Hokuyo URG-04L/UTM-30Lx , Xtion1/2 , Kinect1/2，ZED Stereo Camera , TK1，TX1/2 , 树莓派 , Dobot机械臂 1/2

## 设计特点

<div align=center><img src="/images/Mechanical/stone/Stone_V2.0_turn_around_good.gif"/></div>

前置万向轮的两轮驱动方式让车体拥有优越的稳定性；一对775电机加64mm铝合金轮保证了强大前行动力；三层高强玻纤板加8根铝柱组建的骨架在保证承力可靠性的同时以一种简洁明快的方式将各部件一无保留地呈现给使用者。从此，安装、接线、测试、检修，轻车熟路，一目了然。毫无意外，Stone能够支持多种激光雷达，多种控制器（Tk1、Tx1、树莓派等），也可以支持小型机械臂，如Dobot1、Dobot m1。另外，Stone高置的云台能够兼容多款RGBD摄像头和单、双目摄像头，并能提供270度的周向旋转角和180度的俯仰旋转角，让世界一览无余。

## 套餐价格　

Stone 套餐 | 属性 | 价格(不带发票)
-----|-----|-----
<br>基础版|1. 机械结构(包含云台支杆和云台)<br>2. 控制电路，驱动电路，配套开发调试硬件，电池套装x1<br>3. 技术手册，社区支持，技术交流和指导 (不提供免费教学培训)|<br>3999 RMB
导航低配版|1. 基础版全部内容<br>2. 六代双核酷睿i3工控机，rplidar a1(激光雷达)|6599 RMB
导航中配版|1. 基础版全部内容<br>2. 七代双核酷睿i7工控机，rplidar a1(激光雷达)|8199 RMB
导航高配版|1. 基础版全部内容<br>2. 七代双核酷睿i7工控机，rplidar a2(激光雷达)|9999 RMB
<br>视觉低配版|1. 导航低配版全部内容<br>2. 华硕Xtion2摄像头|<br>8599 RMB
<br>视觉中配版(推荐)|1. 导航中配版全部内容<br>2. 华硕Xtion2摄像头|<br>10199 RMB
<br>视觉高配版|1. 导航高配版全部内容<br>2. 华硕Xtion2摄像头|<br>11999 RMB
<br>定制版|1. 量大可定制<br>2. 任选可支持的传感器，设备，控制器<br>3. 可定制相关服务，如系统配置，**RoboCup比赛指导**<br>4. *定制 导航/任务执行/人脸识别/目标识别/跟踪/机械臂抓取 等功能*|<br> ¥¥¥¥¥ RMB

## [点击购买 Stone](https://item.taobao.com/item.htm?spm=a1z10.3-c.w4002-13224047684.13.1bb37efbrJ1Dfz&id=551103715089)　　  　　　　　　　

## 实验演示

### 基于激光雷达的建图导航避障 (此处采用了Stone的前身Jilong的视频)


<div align=center><img width="600" height="450" src="/images/Experiment/jilong/jilong_navigation_best_compression.gif"/></div>

### 基于RGBD的目标跟踪(此处采用了Stone的前身Jilong的视频)


<div align=center><img width="600" height="450" src="/images/Experiment/jilong/jilong_cvdemo_best_comprssion.gif"/></div>

### 基于RGBD的建图导航避障 


<div align=center><img width="600" height="450" src="/images/Experiment/stone/stone_navigation_best_compression.gif"/></div>

综合来说，Stone已经很好的个人机了，有一定的载重能力，支持Dobot机械臂，适合小实验室和个人机器人研究。但是还不能完成一些复杂的任务，比如抓取一瓶水，开个门，负载也有限，所以有更高需求的请看[Giraffe](/docs/Products/Giraffe.md)，Giraffe有着庞大的身躯和超大的负载能力，可以支持UR5和KUKA的一些工业机械臂，或者配合HandsFree自主设计的低成本ARM，可以胜任大部分的机器人研究任务。


