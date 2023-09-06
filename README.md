# Asus-FX50JX-Hackintosh
My laptop work on hackintosh

## 电脑配置

- CPU Intel i5 4200H
- 显卡：
  - 集显：HD4600
  - 独显：NVIDIA 950M(不可用)
- 内存：4GB板载 + KingSton 4GB DDR3 1333MHz
- 硬盘 Intel 545S 256G SSD
- 网卡：原装蓝牙不可用，更换为BCM943225HMB

### 正常工作
- [x]睡眠&唤醒
- [x]触摸板
- [x]Fn快捷键
- [x]CPU变频
- [x]亮度调节
- [x]HDMI输出
- [x]WIFI&蓝牙
- [x]音频&麦克风

## 参考配置

[参考EFI](https://github.com/jonalinux/Hackintosh-Asus-X550JX)
使用该EFI配置里面的`EFI-ventura.zip`文件

优化后EFI下载地址:[Asus-FX50JX-Hackintosh](https://github.com/SlippyJimmy/Asus-FX50JX-Hackintosh)

安装后，声卡、网卡蓝牙及核显驱动存在问题，下面一一解决

**注：本人OpenCore版本为0.6.1,后续使用OCC保持版本一致**

### 亮度调节
pass

### 声卡驱动
[参考教程](https://github.com/jonalinux/Hackintosh-Asus-X550JX/tree/main)，使用Hackintool将`voodooHDA.kext`安装到`L / E (Library / Extensions)`

### 网卡&蓝牙驱动

若为原装网卡，可使用参考EFI自行测试,如果是更换了其他网卡，可参考下面教程进行驱动

[参考教程](https://www.bilibili.com/video/BV1de4y1X7mp)

网卡蓝牙可以驱动，显示支持隔空投送，但实现不了

### 核显驱动

问题描述：核显仅为7M，画面很卡

[参考教程](http://imacos.top/2022/09/26/2310/)


### CPU睿频

使用工具：CPU-S、Hackintool
[参考教程](https://www.bilibili.com/video/BV143411F7aJ)

### 花屏

问题描述：开机二阶段分裂成8个苹果，进入系统后花屏

解决方案：

1. bios中打开CSM（会导致开机一阶段图标变大的问题）
1. 自定义EDID（待尝试）


