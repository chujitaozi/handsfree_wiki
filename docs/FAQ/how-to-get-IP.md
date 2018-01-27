## 获取工控机IP地址的方案
在进行远程控制之前，我们需要在.bashrc文件里面填写运行Master节点的工控机的IP地址，只有IP地址写对了，两台电脑上的节点才能正常通信。
---
### 方案一：工控机上读取
将工控机接上显示器和键盘，打开终端，输入：
>ifconfig

因为一般工控机是连接的无限网络，所以主要看wlan这边的信息（注意：有些电脑的无线网卡名称不是wlan，而是wlp60s0）。在对应的信息部分找到inet addr：xxx.xxx.xxx.xxx就是对应的IP地址。
---
### 方案二：网页上读取
如果你使用的是无线路由器建立的无线网络，你可以在网页浏览器地址栏输入192.168.1.1，就可以查看到工控机的IP地址。
---
### 方案三：手机上查看
如果你是用手机建立的无线网络，可以在手机上查看工控机的IP地址。