# Stone机器人
## 概述
> 墨雅敦庄，举重若轻

![Alt text](/images/Products/Stone/Stone_V3.jpg)

多功能通用型机器人研究开发平台，内外兼修，集成专业的控制系统，适用于机器人相关领域的研究和产品Demo研发。

## 外形及性能参数

![Alt text](/images/Products/Stone/Stone_V3_Parameter.jpg)

## 设计特点

![Alt text](/images/Products/Stone/Stone_V3_Resource.jpg)

Stone是一款采用前万向后差速驱动底盘布局的中型机器人开发平台。其主体结构由高强度哑黑E-CR玻纤板和2020型磨砂黑铝合金柱螺接而成，使得Stone拥有15Kg载重能力的同时也拥有墨黑儒雅的风度。Stone采用了基于32位STM32F407芯片的多功能控制器OpenRE Board，拥有丰富的板载资源和二次开发接口，还集成了十轴惯性测量单元。Stone搭载Power Manager电源管理系统，在拥有电池充放电保护、过流过压保护、电量显示等功能的同时，还能向外界提供5V、12V和19V的稳定电能输出，让用户摆脱上层设备供电不便的烦恼。Stone的设计从用户角度出发，设计了双急停开关和航空通信插头，在顶部搭载2自由度云台、13.3寸IPS显示器和高保真双音响，让整机布局科学合理，人机交互变得更为简单便捷。一如既往，Stone传承了HFR机器人系列高通用化、高拓展性的血统，可支持多款主流的激光雷达、单板计算机、RGBD摄像头。更不一样的是，Stone支持主流的桌面机械臂，如Dobot、7Bot等，让你玩转桌面应用。Stone支持OpenRE机器人库和ROS系统，完善的开发教程，满足ROS开发、SLAM研究者的需求，适用于机器人相关领域的研究和产品Demo研发。

## 套餐价格　

Stone 套餐 | 属性 | 价格(不带发票)
-----|-----|-----
<br>基础版|1. 机械结构(包含云台支杆和云台)，双音箱<br>2. 控制电路，驱动电路，配套开发调试硬件，电池套装x1<br>3. 技术手册，社区支持，技术交流和指导 (不提供免费教学培训)|<br>5998 RMB
导航低配版|1. 基础版全部内容<br>2. 六代双核酷睿i3工控机，rplidar a1(激光雷达)|8598 RMB
导航中配版(推荐)|1. 基础版全部内容<br>2. 七代双核酷睿i3工控机，rplidar a2(激光雷达)|10398 RMB
导航高配版|1. 基础版全部内容<br>2. 七代双核酷睿i7工控机，rplidar a2(激光雷达)|11998 RMB
<br>视觉低配版|1. 导航低配版全部内容<br>2. 华硕Xtion2摄像头|<br>10598 RMB
<br>视觉中配版|1. 导航中配版全部内容<br>2. 华硕Xtion2摄像头|<br>12398 RMB
<br>视觉高配版(推荐)|1. 导航高配版全部内容<br>2. 华硕Xtion2摄像头<br>3. 13.3寸高清显示屏，无线键鼠，PS3遥控器|<br>15398 RMB
<br>定制版|1. 量大可定制<br>2. 任选可支持的传感器，设备，控制器<br>3. 可定制相关服务，如系统配置，**RoboCup比赛指导**<br>4. *定制 导航/任务执行/人脸识别/目标识别/跟踪/机械臂抓取 等功能*|<br> ¥¥¥¥¥ RMB

## [点击购买 Stone](https://item.taobao.com/item.htm?spm=a1z10.3-c.w4002-13224047684.13.1bb37efbrJ1Dfz&id=551103715089)　　  　　　　　　　

## 实验演示

### 基于激光雷达的建图导航避障 (此处采用了Stone的前身Jilong的视频)


<div align=center><img width="600" height="450" src="/images/Experiment/jilong/jilong_navigation_best_compression.gif"/></div>

### 基于RGBD的目标跟踪(此处采用了Stone的前身Jilong的视频)


<div align=center><img width="600" height="450" src="/images/Experiment/jilong/jilong_cvdemo_best_comprssion.gif"/></div>

### 基于RGBD的建图导航避障 


<div align=center><img width="600" height="450" src="/images/Experiment/stone/stone_navigation_best_compression.gif"/></div>

综合来说，Stone已经很好的个人机了，有一定的载重能力，支持Dobot机械臂，适合小实验室和个人机器人研究。但是还不能完成一些复杂的任务，比如抓取一瓶水，开个门，负载也有限，所以有更高需求的请看[Giraffe](/docs/Products/Giraffe.md)，Giraffe有着庞大的身躯和超大的负载能力，可以支持HandsFree，或者配合Hands机械臂和UR系列的机械臂，可以胜任大部分的机器人研究任务。


