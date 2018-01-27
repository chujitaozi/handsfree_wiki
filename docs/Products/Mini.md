本节介绍Mini机器人的相关参数及Demo.


# Mini机器人

<div align=center><img src="/images/Mechanical/mini/wiki/mini_small_render.jpg"/></div>

## 概述
Mini是一款采用前万向后双驱动轮底盘布局的小型机器人。其整机结构采用平板桁架式透明化设计，外形简约大方，能支持多种激光雷达，TK1、树莓派等主流控制器，可搭载assustion、Kinect1 、Kinect2等深度摄像头。Mini体型小、功能强大、性价比高，非常适合入门者开发研究和多机集群应用研究。

## 外形及性能参数

机器人参数| 值
------------ | -------------
净重(kg) | 2
整体尺寸(mm) | 340x230
负载(kg) | 6
最大速度(m/s) | 1.2
电池容量(mAh) | 12V 5200
续航时间(h) | 8
充电时间(h) | 5
驱动方式 | 两轮差分驱动
电源扩展 | 12V/3A x 2 ,  USB5V/2A x 2
电机控制接口数量 | 4
内部传感器 | 集成编码器，陀螺仪,可扩展超声/红外传感器
通信扩展接口 | USB-USART x 1 , USART x 2, Bluetooth x 1 , CAN x 1 , SPI x 1 
支持安装的设备 | RplidarA1/A2，Hokuyo URG-04L/UTM-30Lx，Xtion1/2，Kinect1/2，TK1，树莓派

## 设计特点

<div align=center><img src="/images/Mechanical/mini/HF_mini_turn_around_medium.gif"/></div>

23cm直径机身，四层黑色哑光玻纤板（亚克力板），9根10mm直径高强铝柱，12v驱动775电机，mini带来的不仅是体型上的小巧玲珑和机械结构的高可靠度，还有出色的动力学性能和别具一格的机械美感。透明化的结构设计使用户的安装、接线、调试、检修顺手简单。麻雀虽小，五脏俱全，Mini小小的体型上能同时支持多种传感器和主流控制器，能运行HandsFree团队开发的任何软件，是初学者入门及多机集群研究、应用的不二选择。

## 套餐价格　　　　　　　　　　　　　　　

Mini 套餐 | 属性 | 价格(不带发票)
-----|-----|-----
<br>基础版|1. 机械结构<br>2. 控制电路，驱动电路，配套开发调试硬件，电池套装x1<br>3. 技术手册，社区支持，技术交流和指导 (不提供免费教学培训)|<br>1999 RMB
导航开发版(推荐)|1. 基础版全部内容<br>2. 赛扬处理器工控机，rplidar a1(激光雷达)|4199 RMB
<br>视觉开发版|1. 导航开发版全部内容<br>2. 华硕Xtion2摄像头|<br>6199 RMB
<br>定制版|1. 量大可定制<br>2. 任选可支持的传感器，设备，控制器<br>3. 可定制相关服务，如系统配置，**RoboCup比赛指导**<br>4. *定制 导航/任务执行/人脸识别/目标识别/跟踪/机械臂抓取 等功能*|<br> ¥¥¥¥¥ RMB

## [点击购买 Mini](https://item.taobao.com/item.htm?spm=a1z10.5-c.w4002-13224047689.15.1ca8e435HCtjBj&id=551101819610)　　  　　　　　　　

## 实验演示
Mini 小巧玲珑，售价底，适合学生入门 和 用于研究多机器人协同。然而Mini虽然小，却五脏俱全，在移动，建图，导航，避障方面的效果并不会比Stone 和 Giraffe 差，只是载重小，不能放机械臂，PC，这样就限制了机器人其他方面的研究，所以需要更高平台需求的可以看[Stone](/docs/Products/Stone.md)和[Giraffe](/docs/Products/Giraffe.md)

### 基于深度强化学习的多机器人去中心化避障实验 by [Dorabot](http://www.dorabot.com/) 

![4-13](/images/Experiment/mini/4_13_best_compression.gif)
![4-14](/images/Experiment/mini/4_14_best_compression.gif)

去中心化的多机器人避障（decentralized multi-robot collision avoidance） 目标在与多机器人系统在没有中心服务器规划，甚至机器人间没有通讯的情况下，也能拥有高效， 无震荡（Oscillation-Free）机器人避障行为。可以类比在拥挤的街道上行走的人们。基于handsfree 我们构建了完善的实验平台，在我们的实验中，handsfree极大减少了底层开发的难度，加速了我们实物机器人实验进程。
