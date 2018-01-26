本节介绍Mini机器人的相关参数及安装.


# Mini机器人

![Alt text](/images/Mechanical/mini/wiki/mini_small_render.jpg)

## 概述
Mini是一款采用前万向后双驱动轮底盘布局的小型机器人。其整机结构采用平板桁架式透明化设计，外形简约大方，能支持多种激光雷达，TK1、树莓派等主流控制器，可搭载assustion、Kinect1 、Kinect2等深度摄像头。Mini体型小、功能强大、性价比高，非常适合入门者开发研究和多机集群应用研究。

## 外形及性能参数
机器人参数| 值
------------ | -------------
空重 | < 2kg
直径(cm)  | 23
高度(cm)|20.4（不加云台） 33.3（加云台）
最大速度(m/s) | 1.2
额定承载能力(kg) |3
支持的传感器 | Rplidar A1/A2，Hokuyo URG-04L/UTM-30Lx，assusxtion，Kinect1/2)
支持的控制器 |  TK1，RK3288，树莓派，pcduino

## 设计特点

![Alt text](/images/Mechanical/mini/HF_mini_turn_around_medium.gif)

23cm直径机身，四层黑色哑光玻纤板（亚克力板），9根10mm直径高强铝柱，12v驱动775电机，mini带来的不仅是体型上的小巧玲珑和机械结构的高可靠度，还有出色的动力学性能和别具一格的机械美感。透明化的结构设计使用户的安装、接线、调试、检修顺手简单。麻雀虽小，五脏俱全，Mini小小的体型上能同时支持多种传感器和主流控制器，能运行HandsFree团队开发的任何软件，是初学者入门及多机集群研究、应用的不二选择。

## 实验演示
Mini 小巧玲珑，售价底，适合学生入门 和 用于研究多机器人协同。然而Mini虽然小，却五脏俱全，在移动，建图，导航，避障方面的效果并不会比Stone 和 Giraffe 差，只是载重小，不能放机械臂，PC，这样就限制了机器人其他方面的研究，所以需要更高平台需求的可以看[Stone](https://github.com/HANDS-FREE/HANDS-FREE.github.io/wiki/4.2-Stone)和[Giraffe](https://github.com/HANDS-FREE/HANDS-FREE.github.io/wiki/4.3-Giraffe)

### 基于深度强化学习的多机器人去中心化避障实验 by [Dorabot](http://www.dorabot.com/) 

![4-13](/images/Experiment/mini/4_13_best_compression.gif)

![4-14](/images/Experiment/mini/4_14_best_compression.gif)

去中心化的多机器人避障（decentralized multi-robot collision avoidance） 目标在与多机器人系统在没有中心服务器规划，甚至机器人间没有通讯的情况下，也能拥有高效， 无震荡（Oscillation-Free）机器人避障行为。可以类比在拥挤的街道上行走的人们。基于handsfree 我们构建了完善的实验平台，在我们的实验中，handsfree极大减少了底层开发的难度，加速了我们实物机器人实验进程。
