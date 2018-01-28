# 开箱组装
在发货时,大部分的组装工作已经完成.本节简单介绍开箱注意事项及连线细节。

机械部分的详细安装，请参考[机器人安装详细步骤](docs/FAQ/Assemble_details.md)。

下面分别是[Mini](/docs/Getting_Started/assemble_robot.html#mini机器人)、[Stone](/docs/Getting_Started/assemble_robot.html#stone机器人)和[Giraffe](/docs/Getting_Started/assemble_robot.html#giraffe机器人)安装时的注意事项和连线细节。
# Mini机器人

### 状态检查
#### 查看机器人状态
开箱之后看到的应该是已经安装好的机体和其他零件。
![底盘](明天加)

![零件](明天加)   
#### 查看上电状态
将电池放置在机器人底层板后面(有凹槽),断电情况下连接电池与主控板和驱动板,然后上电，驱动和主控板灯亮
![底层连接](明天加)

### 注意事项

* 1 Jlink 1个（包括swd线和一根USB）,这部分是用来更新底层板的,暂时用不到
* 2 雷达,A2(A1或其他)雷达是安装在机器人上面的,使用时直接通过USB供电及通信
* 3 工控机通过控制板供电,电源模块都已经集成在底层控制板,单排黑色插孔均可提供12V电压,所以都可以给工控机供电

# Stone机器人

### 状态检查
开箱之后请进行下面几个步骤对机器人进行检查   
#### 查看机器人状态
开箱之后看到的应该是已经安装好的机体和其他零件。
![底盘](/images/Tutorial/Getting_Started/stone_poweroff.jpg)

![零件](明天加)   
#### 查看电池状态
电池发货时应该是断开状态,先将开关断开(向上为断开),然后连接电池与电源管理板,打开开关
![电池](/images/Tutorial/Getting_Started/power.jpg)
#### 查看上电状态
将电池放置在机器人底层板后面(有凹槽),断电情况下连接电池与主控板和驱动板,然后上电，驱动和主控板灯亮
![底层连接](/images/Tutorial/Getting_Started/stone_poweron.jpg)
#### 查看云台状态
按照机械部分的详细安装步骤安装云台。云台通过舵机延长线与主控板直接相连（连接规则：七上八下），并由主控板直接供电。连接时请注意正负极（主控板必须由12V供电，才可以驱动云台）

![云台](明天加)   

### 注意事项

* 1 Jlink 1个（包括swd线和一根USB）,这部分是用来更新底层板的,暂时用不到
* 2 雷达,A2(A1或其他)雷达是安装在机器人上面的,使用时直接通过USB供电及通信
* 3 工控机通过电源管理系统供电,电源管理系统中,单排黑色插孔均可提供12V电压,所以都可以给工控机供电
* 4 急停开关直接和电源管理模块相连,摁下后会断电

如果各部分状态良好，则可以开始进行下一节：[简单使用](/docs/Getting_Started/test_robot.md)。

# Giraffe机器人
Giraffe机器人请参考[Stone机器人](/docs/Getting_Started/assemble_robot.html#stone机器人)。
