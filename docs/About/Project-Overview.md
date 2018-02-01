## HandsFree 组成
项目虽然看起来涉及很广，但目前主要任务大概有三个。      

### 一 OpenRE 库
全称 Open Source Robot Embedded Library，也就是机器人嵌入式库。简单的说，其作用与国外知名的无人机开发架构 pixhawk 类似，只不过 pixhwak 主要是面向飞行器，而 OpenRE 则是面向多模态机器人的。

![OpenRE](/images/OpenRE/Embedded_Architectural.jpg)

> [Download OpenRE](https://github.com/HANDS-FREE/OpenRE)
       
### 二 多模态平台设计
我们的开发项目和开发平台是多样化的，比如二轮，三轮的移动机器人，四旋翼固定翼飞行器等，重复造轮子的问题是机器人学者和创业者最常遇到的问题，好的系统是要求很好的泛性的，能够适应大部分平台，避免了重复劳动的弊端，这就要求我们的产品更加多元化。	在多模态机器人平台搭建方面，研究的主要内容是设计精良的机械和电路系统。机械系统包括各种模型的机器人躯体、机械臂、云台等。电路则包含控制系统，驱动电路，电源管理系统，硬件调试等方面。

![Alt text](/images/About/HandsFree_Introduction/4.jpg)
![Alt text](/images/About/HandsFree_Introduction/8.jpg)

**多模态平台旨在以机器人学，自动化，通信电子和周边知识为支撑，搭建科学、鲁棒、友好、统一的机器人硬件系统，以配合整个软硬件系统的统一**
- 为了促进社区交流，我们开源了大部分的设计资料，请看[百度云](https://pan.baidu.com/s/1nuSvs7Z#list/path=%2FHANDSFREE%2FHands_Free_Release%2F2_Hardware&parentPath=%2FHANDSFREE)
         
### 三 系统搭建
主要是基于前两个任务，结合团队在 SLAM， 物体识别，机器人任务规划等研究，以及国外知名的 ROS 等开源项目，搭建整个机器人系统，实现一些应用。
- 自主移动模块框架搭建
- 物体识别模块
- 机械臂控制模块
- 多机器人协同

[HandsFree Github](https://github.com/HANDS-FREE/handsfree)     

![Alt text](/images/About/HandsFree_Introduction/14.jpg)
![Alt text](/images/About/HandsFree_Introduction/15.jpg)
![Alt text](/images/About/HandsFree_Introduction/16.jpg)

### 总结
我们希望HandsFree 成为一套可以遵循的标准，而不仅仅只是一个工程，所以我们精心制定了电路设计标准和机械设计标准，并且公开了我们团队的PCBLIB和机械模型库，凡是照着这个标准来设计的机器人将会很大程度的兼容HandsFree的软件系统，我们希望此举让更多的机器人研究者得到便利，也希望有心人帮助我们完善这个标准的内容。

### PIL 介绍
西北工业大学布树辉教授的智能系统实验室开发的跨平台软件库 [PIL](https://github.com/HANDS-FREE/PIL )，支持多线程、时钟、插件、网络、常用硬件抽象、计算机视觉、GUI等功能。布老师是我人生中最敬佩导师，他不仅有着超强的工程和科研能力，而且和蔼可亲，亦师亦友，手把手教，更难得的是，他比学生们还要努力，总是走在团队的最前面带着每个学生奋斗，喜欢机器人或者无人机领域的伙伴们可以关注一下他的[个人网站](http://www.adv-ci.com/blog/)，如果想读他研究生或者博士的伙伴也可以来联系群主。   

##  HandsFree开源机器人项目综合介绍

![Alt text](/images/About/HandsFree_Introduction/1.jpg)
![Alt text](/images/About/HandsFree_Introduction/2.jpg)
![Alt text](/images/About/HandsFree_Introduction/3.jpg)
![Alt text](/images/About/HandsFree_Introduction/4.jpg)
![Alt text](/images/About/HandsFree_Introduction/5.jpg)
![Alt text](/images/About/HandsFree_Introduction/6.jpg)
![Alt text](/images/About/HandsFree_Introduction/7.jpg)
![Alt text](/images/About/HandsFree_Introduction/8.jpg)
![Alt text](/images/About/HandsFree_Introduction/9.jpg)
![Alt text](/images/About/HandsFree_Introduction/10.jpg)
![Alt text](/images/About/HandsFree_Introduction/11.jpg)
![Alt text](/images/About/HandsFree_Introduction/12.jpg)
![Alt text](/images/About/HandsFree_Introduction/13.jpg)
![Alt text](/images/About/HandsFree_Introduction/14.jpg)
![Alt text](/images/About/HandsFree_Introduction/15.jpg)
![Alt text](/images/About/HandsFree_Introduction/16.jpg)
![Alt text](/images/About/HandsFree_Introduction/17.jpg)
![Alt text](/images/About/HandsFree_Introduction/18.jpg)
![Alt text](/images/About/HandsFree_Introduction/19.jpg)
![Alt text](/images/About/HandsFree_Introduction/20.jpg)
![Alt text](/images/About/HandsFree_Introduction/21.jpg)
![Alt text](/images/About/HandsFree_Introduction/22.jpg)
![Alt text](/images/About/HandsFree_Introduction/23.jpg)
![Alt text](/images/About/HandsFree_Introduction/24.jpg)
![Alt text](/images/About/HandsFree_Introduction/25.jpg)
![Alt text](/images/About/HandsFree_Introduction/26.jpg)
![Alt text](/images/About/HandsFree_Introduction/27.jpg)
![Alt text](/images/About/HandsFree_Introduction/28.jpg)
![Alt text](/images/About/HandsFree_Introduction/29.jpg)
![Alt text](/images/About/HandsFree_Introduction/30.jpg)
![Alt text](/images/About/HandsFree_Introduction/31.jpg)
![Alt text](/images/About/HandsFree_Introduction/32.jpg)
![Alt text](/images/About/HandsFree_Introduction/33.jpg)
![Alt text](/images/About/HandsFree_Introduction/34.jpg)

