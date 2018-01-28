## 运行roslaunch handsfree_hw handsfree_hw.launch出现问题的解决方案

---

### 可能原因一：串口线没有插好或者PC端占用的COM口不是ttyUSB0
**解决办法：**确保只有单片机的USB线插在工控机上，拔掉激光、摄像头的USB线。打开一个终端，输入：
>ls /dev/ttyUSB*

如果显示的USB设备不是ttyUSB0，则拔掉所有USB线，重新插入PC，再次检查是否为ttyUSB0设备号。

---

### 可能原因二：权限不够，不能打开USB口进行通信
**解决办法：**使用以下命令修改ttyUSB0的权限：
> sudo chmod 777 /dev/ttyUSB0

---

### 可能原因三：主控板中的固件烧写不正确
由于版本差异等原因，固件烧写错误会导致通讯错误，出现timeout错误。
**解决办法：**根据移动底盘的型号、OpenRe的版本和Hnads-Free ROS代码的版本重新选择固件进行烧写。

---

### 可能原因四：没有改程序中的路径
handsfree的源码clone下来之后，要去**handsfree/handsfree_hw/src/main.cpp**里面把**"/home/luyifan/handsfree_ws/src/handsfree/handsfree_hw/config.txt")**改成自己的电脑里面对应的路径，再重新编译。
