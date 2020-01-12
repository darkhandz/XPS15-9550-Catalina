### 一些说明

这里只分享我自己目前在用的配置，不一定适合你，可以参考，修改成自己合用的。

这套配置是我10.15.2用的，在全新安装的情况下请自行测试下，可能会需要你用外置鼠标。

> 请不要开启`filevault`，我完全没有用过这个功能，你有需要的话，自己重新安装一下Clover。

Clover是`r5102`版本，安装参考文末设置, [这里有下载](https://github.com/CloverHackyColor/CloverBootloader/releases)


### 硬件配置

- 机型：DELL XPS15 9550
- BIOS：v1.11.2
- CPU：Intel i7 6700HQ
- 内存：16G DDR4 2400（原厂8G，自己换了）
- 硬盘：SM961 256G NVMe SSD
- 核显：HD530, 1920x1080
- 声卡：Realtek ALC298（也叫ALC3266）
- 无线网卡：DW1830（带蓝牙）

DW1830我是机器原配的，如果你要另外买，建议考虑下DW1560或DW1820a，买之前自己了解下是否可以完美使用，另外BCM94360CS2+转接延长线也可以考虑。

### 安装完之后的一些问题

- 独显不指望了
- 无线5GHz达不到最高速度（我没具体测试过）
- ThunderBolt没设备测试
- USB-C的扩展坞在睡眠唤醒之后需要再拔插一次
- 低亮度会有轻微闪屏
- 睡眠唤醒后AirDrop可能搜索不到设备，关闭WiFi再打开就可以了

### 耳机拔插(Other/ComboJack)

我个人没什么耳机需求，所以在10.15.2没有安装这个东西了，请自行测试。

它的作用：检测耳机拔插，修复耳机孔多合一下产生的一些问题，关于它的原理，请看[wmchris的教程](https://github.com/wmchris/DellXPS15-9550-OSX/blob/master/10.12/Post-Install/AD-Kexts/Audio/VerbStub_knnspeed/README.md)。

- 执行命令：`cd 把ComboJack文件夹拖过来`
- 执行命令：`chmod +x install.sh`
- 执行命令：`./install.sh`
    
    ![](http://darkhandz.qiniudn.com/2017-11-03-132202.png)

看见`Enjoy!`的话，ComboJack就安装完成了，重启一下系统。


### Clover 安装参考

![安装选项](https://github.com/darkhandz/XPS15-9550-Catalina/blob/master/Clover_Install.jpg)
