### Linux文件与目录结构
Linux系统中一切皆文件

Linux目录结构：

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753103209101-a4e96a2e-c20d-4a01-ba9c-08cc149ba3e1.png)

### VIM编辑器
vi\vim是visual interface的简称, 是Linux中最经典的文本编辑器同图形化界面中的文本编辑器一样，vi是命令行下对文本文件进行编辑的绝佳选择。

vim 是 vi 的加强版本，兼容 vi 的所有指令，不仅能编辑文本，而且还具有 shell 程序编辑的功能，可以不同颜色的字体来辨别语法的正确性，极大方便了程序的设计和编辑性。

VIM的三种模式

命令模式（Command mode）: 命令模式下，所敲的按键编辑器都理解为命令，以命令驱动执行不同的功能。此模式下，不能自由进行文本编辑。

输入模式（Insert mode）:也就是所谓的编辑模式、插入模式。此模式下，可以对文件内容进行自由编辑。

底线命令模式（Last line mode）:以：开始，通常用于文件的保存、退出。

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753105781401-67afeac3-f584-4199-ab0c-8b2b4b14d39e.png)

#### 编辑模式
![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753106085470-0748d941-fb99-4a63-906f-9ebb2f2d99d5.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753107454464-a733192f-c7a3-4a24-92ae-af2b07c2fc46.png)

复制多行：y+num+y / num +yy

删除多行：d+num+d / num +dd

复制从当前光标到列尾：y$

复制从当前光标到列首：y^

删除从当前光标到列尾：d$

复制从当前光标到列首：d^

以词为单位复制(从光标到词尾)：yw

以词为单位删除(从光标到词尾)：dw

剪切：x

退格键：shift+x

修改单个字符：r

修改多个字符：shift+r

调到上一个词：b

调到下一个词：w

调到文档开头：gg / shift+h

调到文档结尾行：shift+g / shift+l

**: set nu 设置显示行号**

**: set nonu 设置隐藏行号**

#### 一般模式
![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753145536410-e14d9950-3af2-47cd-9501-e82141ad0bdf.png)

#### 命令模式
![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753145923200-609bb979-6df9-4a30-9119-8cdf5b2a1bca.png)

**注意点：**

:s/old/new/ 默认只对当前行进行替换。如果当前行没有 "old" 这个字符串，就会报<font style="color:rgb(6, 7, 31);background-color:rgb(253, 253, 254);">找不到模式的</font>错。

### 网络配置
#### 查看网络IP和网关
##### 查看虚拟网络编辑器
![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753194975780-88c53d7c-7557-4525-af90-2fbc04127c3d.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195177816-d1e92248-35ee-406b-bd84-6daec499be21.png)

 ![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195236108-4b5364d8-b4e3-4b61-b015-dae887510520.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195332040-1c2795ed-d46c-4c4b-b237-030aba112916.png)

虚拟机和主机ip前缀不一致，是因为本质上是两个局域网下的网络。

本来主机也是访问不到虚拟机的，就类似于访问外网的其他电脑只知道主机的ip但不知道主机所在局域网中的地址。

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195578949-b7187899-e3f7-432d-b01e-9f48d6ec6d31.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195606875-f988730b-760d-4c9a-b89c-7b61a2adf330.png)

VMware就设置一个类似网卡的设备，连接到虚拟机所在局域网中的路由器，进而连接到虚拟机。

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195798732-b6246115-f484-440b-9d1b-8a3a48dbfa5a.png)

这里指的是**仅主机模式**时使用的

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753195895634-1ddff920-a842-433e-b779-51e334fdad68.png)

#### 修改静态ip
动态ip重启后会动态改变，集群管理等复杂，所以需要更改为静态ip。



注意：虚拟机每次开机都没网络

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753232879983-b0d95516-3ae6-49fb-a9e3-c86054f6c003.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753315377642-e4504448-4bc9-45e0-a275-6b347fb93c27.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753232905429-6c036d64-8838-46b9-bc7e-9b181939d2d9.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753232926317-608f52d1-b377-418d-864e-927f9276f8f6.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753315402274-10609087-9d09-4676-a99f-0a868a657071.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753233008397-6b643bff-7a41-468c-bbff-77a9258fe934.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753233037002-355b6cfd-b582-4a1d-bcf9-d035a6af5dfc.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753315452156-4df57bad-b7d1-41c2-828c-a9b7fd6bd89b.png)

修改：<font style="color:rgb(25, 27, 31);">vi /etc/sysconfig/network-scripts/ifcfg-ens33</font>

<font style="color:rgb(25, 27, 31);">如果ONBOOT字段为no，需要将其改为yes，该字段表示该网卡是否开机自启。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753233702269-bcc1cc79-7494-4dc5-a5a4-e64720cffa8d.png)

<font style="color:rgb(25, 27, 31);">重启网卡服务：systemctl restart network</font>

#### 设置主机名
vim /etc/hostname

这种方式每次都要重启生效

hostnamectl set-hostname hadoop100

即可

设置类似于通讯录的配置文件hosts，主机名与ip映射的文件

vim /etc/hosts

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753317614177-0b39135e-a289-41fc-a5b4-eeb05b044587.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753317775521-247981ce-89d8-4e4c-b0d9-0b51f11e775a.png)

修改好虚拟机的hosts

也要修改主机的hosts，使主机也可以‘认识’，通过主机名访问

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753317938717-4e698863-dc9a-4bf4-9b44-15fa375cc4d7.png)

测试效果：

主机ping虚拟机

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753317986831-8e5363f1-9199-4a1e-9d95-406f7d1bb675.png)

#### 远程连接
主机连接虚拟机

管理员启动cmd

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753318351855-f8322a56-a741-4b63-9552-6b9fc6bb61af.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753318416147-4c5cc9a5-39fc-4aff-809d-edce8ecb4107.png)

### 系统管理
ls /usr/sbin/ | grep service   查看服务

计算机中，一个正在执行的程序和命令，就被叫做进程；

启动之后一直存在、常驻内存的进程，被称作服务。

守护进程就是Windows中的服务。

#### systrmctl
##### 基本语法
systrmctl start | stop | restart | status

##### 经验技巧
查看服务的方法：/usr/lib/systemd/system 

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753585106324-65860129-0916-4cd9-adaf-61125b1b7ad5.png)

#### 系统运行级别
Centos6：

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753585615860-37acafed-c03e-4334-809c-7e79f401bf93.png)

![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753585751127-1031b64b-ea74-4a72-9400-8ae028f9321f.png)

#### 关机重启
![](https://cdn.nlark.com/yuque/0/2025/png/47441741/1753586985325-98cae525-7a60-4a03-a521-c12b17e894a4.png)



