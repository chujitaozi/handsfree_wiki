# 4.3 Giraffe

![Alt text](/images/Mechanical/giraffe/good/Giraffe_big_render1.JPG)
![Alt text](/images/Mechanical/giraffe/good/Giraffe_big_render2.jpg)

## 概述
Giraffe是一款采用前万向后双驱动轮底盘布局的智能车平台。其整机结构采用平板桁架式封闭式设计；侧板采用带磁吸可开合设计；传动系统采用同步带传动。Giraffe可同时支持一前一后两个激光雷达，兼容TX1、TK1、树莓派等主流控制器，配备高度可调、能兼容多款RGBD摄像头和单、双目摄像头的两轴云台。Giraffe可搭载HF Arm1等中型机械臂（总量15Kg左右），具有高达30Kg的承载能力。

## 外形及性能参数
机器人参数| 值
------------ | -------------
空重 | < 12kg
直径(cm) | 38
高度(cm) | 33.2（不加云台） 126.2（加云台）
最大速度(m/s) | 1.6
额定承载能力(kg) | 30 kg
支持的传感器 | Rplidar A1/A2，Hokuyo URG-04L/UTM-30Lx，assusxtion，Kinect1/2)
支持的设备 | HandFree arm，Dobot机械臂 1/2，HF云台，双目摄像头，单目高清摄像头
支持的控制器 |  笔记本，TX1，TK1，RK3288，树莓派，pcduino

## 实验演示

Giraffe在建图导航避障方面的效果和Stone Mini一样，这里就主要展示一下大型机械臂的3D运动规划和抓取，Giraffe是目前HandsFree功能最全，性能最强的平台，也是HandsFree Team目前研究机器人领域的主要实验平台。

![](/images/Experiment/giraffe/giraffe_grab_best_compression.gif)

## 设计特点

![Alt text](/images/Mechanical/giraffe/HF_Giraffe_turn_around_medium.gif)

全身通体的黑色让Giraffe像黑衣武士一样暗暗地透露出一股邪酷。全封闭式的结构让其有一种不可言状的神秘。不过不要担心，Giraffe的左右侧板和后侧板皆采用了门式的开合结构。门侧采用了磁吸设计，让门的开合变得随意起来，从而让用户能轻易地走进这个黑武士的“内心”，感受其精细的内在。传动系统中同步带的传动方式使电机能精确地将转动位移传递给轮轴，也优化了底盘承力形式，使Giraffe拥有多达30公斤的载重能力。Giraffe能够同时支持前后两个激光雷达，同时能兼容多种控制器（Tk1、Tx1、树莓派等）。健壮的身板使其能够搭载大、中型机械臂，从而使其更具实用能力。高高立起地云台是它不屈的头颅，也给它赢得了“Giraffe（长颈鹿）”这一名号。这个“头颅”上可以支持多款RGBD摄像头和单、双目摄像头，使其能轻易而精确扑捉到自己“指尖”的动作，完成主人交给它的各项指令。

### 安装步骤

![Alt text](/images/Mechanical/giraffe/wiki/giraffe_small_introduction2.jpg)
![Alt text](/images/Mechanical/giraffe/wiki/giraffe_small_introduction1.jpg)
![Alt text](/images/Mechanical/giraffe/wiki/giraffe_small_introduction3.jpg)

### 零件清单
1. 玻纤板十块：底板、中层板、顶板、云台支撑板、激光雷达转接板（2个）、侧缘板（4个）；亚克力板四块：前侧板、左侧门、右侧门、后侧门。
2. 万向轮一套，铝合金轮两套，电机（含减速组和固定架）两套，轮轴两根，轴承座4个，同步带轮4个，同步带两条。
3. 铝柱32根，铝杆2根（选购）、云台一套（选购）
4. 螺钉、螺母若干（考虑到螺钉、螺母为细小部件，易丢失损耗，特意多配几个以作备用）。
