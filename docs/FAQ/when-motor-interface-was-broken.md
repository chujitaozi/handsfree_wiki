##电机接口插拔损坏方案
OpenRE的灵活性之一体现在对硬件资源的快速简单配置。我们的主控板拥有四个电机接口，当我们其中某个电机接口插拔损坏后，可以转而使用其他未被占用的预留电机接口。

具体步骤如下：

- ###更改makefile

1.进入文件夹.../OpenRE/0_Project/makefile路径下，打开*configuration.mk*文件。

2.找到如下代码：
>####select the motor interface of the control_unit_board for robot motor id : motor1, motor2, motor3, motor4  
ROBOT_MOTOR1 ?= motor_interface_1
#### Tips: this means to map motor_interface_1 on the board to No.1 motor of robot
ROBOT_MOTOR2 ?= motor_interface_2
ROBOT_MOTOR3 ?= motor_interface_3
ROBOT_MOTOR4 ?= motor_interface_4

*"ROBOT_MOTOR1"*就是电机一，*"motor_interface_1"*就是板子上的电机接口一。

如果电机接口一插拔损坏，假设只有电机接口一和电机接口二使用，那么只需要将

>ROBOT_MOTOR1 ?= motor_interface_1
>ROBOT_MOTOR3 ?= motor_interface_3

修改为

>ROBOT_MOTOR1 ?= motor_interface_3
>ROBOT_MOTOR3 ?= motor_interface_1

即可。

- ###更改电机到板子上的接口

当我们如上述在makefile文件中修改了电机的接口后，我们只需要将电机一接到板子上的电机接口三上即可。
![Alt text](/images/Hardware/OpenRE_Board/OpenRE_Board_Overview.jpg)
control_unit_v2板如上图所示，电机接口在图右的4,5,8,9接口。
![Alt text](/images/Hardware/OpenRE_Board/OpenRE_Board_Mini_Overview.jpg)
control_unit_mini板如上图所示，电机接口在图右的7,8,9,10接口。