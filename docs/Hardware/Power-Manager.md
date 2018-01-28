## HandsFree Power Manager 使用手册

### 简介
HandsFree Power Manager是HandsFree Team根据HandsFree开源项目的硬件标准设计的一款电源分配板，附带多路开关和多路电源转换功能，满足机器人多样的电力需求。支持常用的TX1/2，TK1，MiniPC，树莓派，Kinect1/2，HOKUYOU雷达，工控机，笔记本等设备供电，同时还支持HandsFree机器人的电机驱动，云台，机械臂,升降等结构的供电，还自带一路急停电源输出。配合大容量电池可以为机器提供集成供电方案。

### 集成供电方案
HandsFree 在中型及以上的移动平台上采用集成化的供电方案，这是为了简化机器人的开发，同时方便开发者进行多种形式自定义需求。在电源板上有数量众多的电源接口，提供多种不同的电压，可以给各种形式的设备进行供电。同时我们统一定义了不同接口和电压的标准，保证了设备的安全。

![Power_Manager](/images/Hardware/HandsFree_Power_Manager/Power_Manager.jpg)

### 板载资源

1. 电源电压 12V ～ 36V
2. USB5V/2A x 2 , 可用于给树莓派，Pcduino等设备供电。
3. 12V/3A x 4 ,  可用于给TK1, Kinect1/2，Hokuyo 雷达等供电。
4. 19V/3A x 3 , 总功率57W以上,可用于给笔记本,工控机等设备供电。
5. 电源扩展/(>10A) x 5 ,电压等于电池电压，其中包含一路急停接口, 可用于给底盘, HandsFree机械臂等供电。
6. HandsFree自带的设备都将支持电源分配板。
7. 购买HandsFree平台将附赠电源分配板的转接线, 用户可以方便的给常用设备供电, 比如PC，TK1,TX1/2等。

![Power_Manager_Overview](/images/Hardware/HandsFree_Power_Manager/Power_Manager_Overview.jpg)

