## OpenRE环境配置
 
本将介绍如何在ubuntu下，配置OpenRE的开发环境，并烧写测试代码。

### 安装
关于工具链的配置有两种方式，可以直接用apt-get 安装，如果网速太慢也可以在百度云下载deb包安装。

首先下载最新的代码：
```
 git clone https://github.com/HANDS-FREE/OpenRE      
```

#### 方法一:  通过deb包安装 

```
$ sudo add-apt-repository ppa:terry.guo/gcc-arm-embedded  
$ sudo apt-get update          
$ sudo apt-get install openocd  gcc-arm-none-eabi    
$ sudo usermod -a -G dialout $USER    
$ sudo apt-get install lib32ncurses5 libtool libusb-1.0 libftdi-dev python python-serial python-empy libpython2.7:i386    
$ sudo apt-get remove modemmanager    
```

#### 方法二:  通过源码安装 (推荐方法) 
- 获取编译工具链的源码 [Development_Toolchain](https://pan.baidu.com/s/1dekYQU#list/path=%2FHandsFree%2FHands_Free_Release%2F3_Software%2FEmbedded_Development_Toolchain&parentPath=%2FHandsFree) ，把下载的源码包放在 OpenRE/5_Development_Toolchain.  或者直接执行命令

```
cd OpenRE & git clone git@github.com:HANDS-FREE/5_Development_Toolchain.git
```
获取到编译工具链的源码

然后一步步执行以下命令，安装好编译工具链。

```
$ cd 5_Development_Toolchain 
$ tar -jxvf gcc-arm-none-eabi-5_4-2016q2.tar.bz2
$ tar -jxvf openocd.tar.bz2
$ tar -jxvf stlink.tar.bz2
$ cd openocd/
$ ./configure
$ make clean
$ make
$ cd ../stlink/
$ make clean
$ make
$ cd ../
$ sudo usermod -a -G dialout $USER      
$ sudo apt-get install lib32ncurses5 libtool libusb-1.0 libftdi-dev python python-serial python-empy libpython2.7:i386     
$ sudo apt-get remove modemmanager    
```

### 代码编译与烧写预备
HandsFree目前有几款不同的主控器，比如用于Stone机器人的control_unit_v2，和用于Mini机器人的control_unit_mini，用jlink烧写时，由于不同的电路板外部晶振频率可能不一样，所以把A板的固件烧到B板就可能导致死机和芯片死锁，板子程序无法跑并且下一次烧写的时候就烧不进了，当出现这种情况的时候，解决方法就是按下板子的复位键(按住不动)，运行烧写指令，一两秒后，松开复位键，就能烧写进去了。

为了确保你不会烧写错误，你先确保每个工程的makefile文件和你的板子是匹配的。这里先介绍每个工程的makefile怎么设置，下一篇会详细介绍整个库的makefile。

一个工程的makefile示例：

```
######################################define project name, board type, and path

#####ROBOT_MODEL : null mini stone stone_omni3 giraffe   
ROBOT_MODEL     ?= stone
#####BOARD_TYPE: control_unit_mini control_unit_v2
BOARD_TYPE      ?= control_unit_v2
#####project name
PROJECT         =  robot_$(ROBOT_MODEL)_$(BOARD_TYPE)
TOP_PATH        =  ../../../..

#############################################################parameters

#####ROBOT_SIMULATION_MODE  : enable disable . enable this mode then you don't need a real robot.
ROBOT_SIMULATION_MODE ?= disable
#####BOOTLOADER  : enable disable
BOOTLOADER_MODE ?= disable

##########################################################################source

CXX_SRC         += ../src/main.cpp 

#Includes
INCDIR          += -I. -I../src/ 

#########################################################################package

#PAKG: common robot_abstract math imu .....
PAKG        = common robot_abstract math imu motor sbus_ppm servo \
              robot_control hf_link tf
              
#OS_MODULE: UCOSII UCOSIII GUI FAT
OS_MODULE  =           

#LIB_MODULE: EIGEN MATRIX  etc
THIRDPARTY_MODULE = 

###################################################################include rules

include $(TOP_PATH)/0_Project/makefile/compiler.mk

```

等号左边的是变量，等号右边的是变量值，#是注释行，注释后面部分是变量的可选值。接下来介绍每一个变量的含义。
* BOARD_TYPE：电路板型号，可选值是HandsFree生产的几款电路板（目前是两款，control_unit_mini、control_unit_v2）。
* ROBOT_MODEL：是使用的机器人的型号，可选值是HandsFree发布的几款机器人，（mini、stone、stone_omni3、giraffe、null代表本工程和机器人对象无关，在跑OpenRE示例教程程序的时候会使用到null）。
* ROBOT_SIMULATION_MODE：仿真模式使能，如果enable，将不需要实体机器人，我们在程序内部虚拟电机模型。一般情况下都选择disable。
* BOOTLOADER_MODE：BOOTLOADER模式可以让用户直接从串口下载程序，如果disable就需要用jlink下载。目前默认disable。
* PAKG：代表本程序所需要使用到的功能包，在简单测试代码里，只用到了common包。在机器人工程实现代码里，用到了就相对较多了。如果不是自己开发程序，该部分内容一般不做修改。
* OS_MODULE：操作系统的模式，目前支持UCOSII、UCOSIII。如果裸跑单片机程序，就空着不填。
* THIRDPARTY_MODULE：第三方库的选择，比如矩阵库之类的，如果使用到就在这里填上对应的第三方库名称。

在正式烧写前，请确保你之前的makefile都配置对了，主要是ROBOT_MODEL，BOARD_TYPE这两个变量，如若配置不对，将有可能发生芯片死锁。

> 以下正式开始编译烧写OpenRE，请确保你打算学习底层嵌入式的开发，HandsFree出厂时都已经烧写好了对应的机器人的固件，以下的学习过程将会覆盖掉出厂程序。

### 烧写一个流水灯的代码测试

> cd OpenRE/0_Project/examples/handsfree_simple_app/linux
* 按照上一步修改makefile。
* 插上jlink同时用usb为板子供电。
* 接着编译：
> make clean
> make
* 最后烧录：
> make burn

烧写成功的现象是，板子上的led灯持续闪烁。

如果使用的是STLink,则需要在make burn之前更改0_Project/makefile/flash.mk
如下:

```
ifeq "$(strip $(BOOTLOADER_MODE))" "enable"
BURN_TYPE       	= usbttl_bootloader_upload 
else
# (stlink/swd/jlink)_(stlink/openocd)_flash  "device"_"driver"_flash
BURN_TYPE      	 	= swd_openocd_flash
DEBUG_TYPE		= swd_openocd_debug
ERASE_TYPE		= swd_openocd_erase
endif
```
改成:

```
ifeq "$(strip $(BOOTLOADER_MODE))" "enable"
BURN_TYPE       	= usbttl_bootloader_upload 
else
# (stlink/swd/jlink)_(stlink/openocd)_flash  "device"_"driver"_flash
BURN_TYPE      	 	= stlink_openocd_flash
DEBUG_TYPE		= stlink_openocd_debug
ERASE_TYPE		= stlink_openocd_erase
endif
```

*（注：如果是重复烧录同一份代码，从第二遍开始就可以省去make clean和make步骤，直接make burn。但是如果两次烧录之间，有.h头文件被修改，就要先make clean，再make，最终make burn。）*

### 烧写机器人的固件程序

固件程序有两个版本的,分别是有操作系统版和裸机版本的,裸机版本是稳定版,操作系统版经过测试也是可以正常使用的.如果你不懂,那么推荐使用裸机版本.

裸机版: 0_Project/firmware/handsfree_wheel_robot     
操作系统版: 0_Project/firmware/handsfree_wheel_robot_ucosIII     

烧写方法和上面一样,值得注意的是,要首先更改Makefile,选择不同的机器人与主控的方式

主要就是修改如下两个变量:

```
#####BOARD_TYPE: control_unit_mini control_unit_v2
BOARD_TYPE		?= control_unit_v2
#####ROBOT_MODEL : null stone stone_omni3 giraffe   
ROBOT_MODEL     ?= stone
```

一个是选择电路板的型号，一个是选择机器人的型号。可选项在makefile里面都以注释的形式标示出来了。    
Stone, Stone Omni3 , Giraffe机器人平台使用的是control_unit_v2控制器, Mini机器人使用的是control_unit_mini.     

这两个变量是必须要选对的,否则会出现意外,比如死锁控制器,或者烧错机器人的代码,导致运动控制不正常.

*（注：非嵌入式开发者只需看到这里即可，想深入开发OpenRE的可以继续研究后面的OpenRE教程）*
