本节介绍Girafee机器人的相关参数及Demo.

# Giraffe机器人

![Alt text](/images/Mechanical/giraffe/good/Giraffe_big_render1.JPG)
![Alt text](/images/Mechanical/giraffe/good/Giraffe_big_render2.jpg)

## 概述
Giraffe是一款采用前万向后双驱动轮底盘布局的智能车平台。其整机结构采用平板桁架式封闭式设计；侧板采用带磁吸可开合设计；传动系统采用同步带传动。Giraffe可同时支持一前一后两个激光雷达，兼容TX1、TK1、树莓派等主流控制器，配备高度可调、能兼容多款RGBD摄像头和单、双目摄像头的两轴云台。Giraffe可搭载HF Arm1等中型机械臂（总量15Kg左右），具有高达30Kg的承载能力。

## 外形及性能参数

机器人参数| 值
------------ | -------------
净重(kg) | 15 (不含机械臂)
整体尺寸(mm) | 420x380x1200
负载(kg) | 50
最大速度(m/s) | 1.2
电池容量(mAh) | 24V 20000
续航时间(h) | 12
充电时间(h) | 6
驱动方式 | 两轮差分驱动
电源扩展 | 19V/3A x 3 , 24V/10A x 5 , 12V/3A x 4 , USB5V/2A x 2 , 一路急停24V/10A
电机控制接口数量 | 4
内部传感器 | 集成编码器 , 陀螺仪 , 磁力计 , 气压计 , 可扩展超声/红外传感器 
通信扩展接口 | USB-USART x 1 , USART x 2, Bluetooth x 1 , CAN x 1 , SPI x 1
支持安装的设备 | RplidarA1/A2，Hokuyo URG-04L/UTM-30Lx , Xtion1/2 , Kinect1/2，ZED Stereo Camera , TK1，TX1/2 , 树莓派 , Dobot机械臂 1/2 , HandsFree机械臂

## 设计特点

<div align=center><img  src="/images/Mechanical/giraffe/HF_Giraffe_turn_around_medium.gif"/></div>

全身通体的黑色让Giraffe像黑衣武士一样暗暗地透露出一股邪酷。全封闭式的结构让其有一种不可言状的神秘。不过不要担心，Giraffe的左右侧板和后侧板皆采用了门式的开合结构。门侧采用了磁吸设计，让门的开合变得随意起来，从而让用户能轻易地走进这个黑武士的“内心”，感受其精细的内在。传动系统中同步带的传动方式使电机能精确地将转动位移传递给轮轴，也优化了底盘承力形式，使Giraffe拥有多达30公斤的载重能力。Giraffe能够同时支持前后两个激光雷达，同时能兼容多种控制器（Tk1、Tx1、树莓派等）。健壮的身板使其能够搭载大、中型机械臂，从而使其更具实用能力。高高立起地云台是它不屈的头颅，也给它赢得了“Giraffe（长颈鹿）”这一名号。这个“头颅”上可以支持多款RGBD摄像头和单、双目摄像头，使其能轻易而精确扑捉到自己“指尖”的动作，完成主人交给它的各项指令。

## 套餐价格　购买

Giraffe 套餐 | 属性 | 价格(不带发票)
-----|-----|-----
<br>基础版|1. 机械结构(底盘 + 云台，不含机械臂)<br>2. 控制电路，驱动电路，开发调试硬件，电池套装x1<br>3. 技术手册，社区支持，技术交流和指导(不提供免费教学培训)|<br>9999 RMB
<br>视觉低配版|1. 基础版全部内容<br>2. 七代双核酷睿i7工控机<br>3. rplidar a2(激光雷达)<br>4. 华硕Xtion2摄像头|<br>17999 RMB
<br>视觉中配版(推荐)|1. 基础版全部内容<br>2. 七代四核酷睿i5HQ + SSD + GTX1060工控机<br>3. rplidar a2(激光雷达)<br>4. 华硕Xtion2摄像头|<br>22999 RMB
<br>视觉高配版|1. 基础版全部内容<br>2. 七代四核酷睿i5HQ + SSD + GTX1060工控机<br>3. Hokuyo UTM-30Lx(激光雷达)<br>4. 华硕Xtion2摄像头<br>5. 可提供RobotCup，RoboMasters等比赛的指导|<br>67999 RMB
<br>定制版|1. 任选可支持的传感器，设备，控制器<br>2. 可定制相关服务，如系统配置，**RoboCup比赛指导**<br>3. *定制 导航/任务执行/人脸识别/目标识别/跟踪/机械臂抓取 等功能*|<br> ¥¥¥¥¥ RMB
定制机械臂|1. HandsFree 机械臂|100000 RMB

## [点击购买 Giraffe](https://item.taobao.com/item.htm?spm=a1z10.5-c.w4002-13224047689.15.2bba683f0Wd2um&id=556483991125)　　  　　　　

## 实验演示

Giraffe在建图导航避障方面的效果和Stone Mini一样，这里就主要展示一下大型机械臂的3D运动规划和抓取，Giraffe是目前HandsFree功能最全，性能最强的平台，也是HandsFree Team目前研究机器人领域的主要实验平台。

<div align=center><img width="600" height="450" src="/images/Experiment/giraffe/giraffe_grab_best_compression.gif"/></div>

