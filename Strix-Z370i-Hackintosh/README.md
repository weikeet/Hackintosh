# Strix-Z370i-UHD630/RX570 for macOS

## Hardware Configuration

| 硬件   | 型号                                       | 价格            | 入手         |
| ------ | ------------------------------------------ | --------------- | ------------ |
| CPU    | i7 8700K                                   | ￥2153          | 天猫         |
| 主板   | Asus ROG Strix Z370-i                      | ￥1649          | 京东         |
| 内存   | 影驰 8GB DDR4 3000MHz                      | ￥484           | 天猫         |
| 固态   | Crucial BX300 240GB<br>Samsung PM981 256GB | ￥324<br>￥543  | 京东<br>天猫 |
| 显示器 | AOC LV273HUPX 27英寸4K                     | ￥1949          | 京东         |
| 电源   | 全汉 MS450 SF电源                          | ￥369           | 京东         |
| 散热   | 利民APX100RH<br>暴力熊散热硅脂             | ￥297<br>￥39.8 | 京东<br>天猫 |
| 机箱   | 屌丝伯 U1 Plus                             | ￥344           | 京东         |
| 线材   | 飞利浦 DP线1.2版 4K高清线                  | ￥52            | 京东         |

## Getting-Started
* HighSierra无法安装在PM981上，看大家都说无法正常在10.13上工作，理论上10.14也该也还是不可以，我是安装在BX300上的
* 机型设置为iMac19.1(独立显卡), Macmini8,1(集成显卡)
* UHD630在10.14.1原生驱动，不需要添加任何驱动，也不需要在Clover配置，睡眠DP音频都没问题
* 声卡驱动使用[AppleALC](https://github.com/vit9696/AppleALC)+[Lilu](https://github.com/vit9696/Lilu)，Clover注入ID 5

## BIOS settings

### Disable

| 英文                                 | 中文                                                     |
| ------------------------------------ | -------------------------------------------------------- |
| Fast Boot                            | 快速启动                                                 |
| CFG Lock (MSR 0xE2 write protection) | CFG 锁 (MSR 0xE2 写入保护)                               |
| VT-d                                 | [VT-d](https://zhidao.baidu.com/question/495526512.html) |
| CSM                                  | 兼容性支持模块                                           |
| Intel SGX                            | Intel SGX                                                |

## Enable

| 英文                    | 中文                                                     |
| ----------------------- | -------------------------------------------------------- |
| VT-x                    | [VT-x](https://zhidao.baidu.com/question/495526512.html) |
| Above 4G decoding       | 大于 4G 地址空间解码                                     |
| Hyper Threading         | 处理器超线程                                             |
| Execute Disable Bit     | 执行禁止位                                               |
| EHCI/XHCI Hand-off      | 接手 EHCI/XHCI 控制                                      |
| OS type: Windows 8.1/10 | 操作系统类型: Windows 8.1/10                             |
| Legacy RTC Device       | 传统 RTC 设备                                            |

### Z370i

#### Ai Tweaker

Ai Tweaker - Ai 智能超频 [XMP]

Ai Tweaker - XMP [XMP DDR4-3000 16-18-18-38-1.35v]

Ai Tweaker - 内存频率 [3200MHz]



#### 高级

高级 - CPU 设置 - 超线程技术 [开启]

高级 - CPU 设置 - 开启处理器核心 [全部]

高级 - CPU 设置 - 硬件预取 [开启]

高级 - CPU 设置 - Intel Virtualization Technology [关闭] -> [开启]

高级 - CPU 设置 - SW Guard Extensions(SGX) [Software Controlled] -> [关闭]

高级 - CPU 设置 - CPU-Power Manager Control - CPU C-states [Auto]

高级 - CPU 设置 - CPU-Power Manager Control - CFG Lock [关闭]



高级 - 北桥 - VT-D [开启] -> [关闭]

高级 - 北桥 - 大于 4G 地址空间解码 [关闭] -> [开启]

高级 - 北桥 - 显示设置 - 首选显卡 [Auto]

高级 - 北桥 - 显示设置 - 初始化 iGPU [关闭] -> [开启]

高级 - 北桥 - 显示设置 - DVMT Pre-Allocated(需要开启 iGPU) [64MB]

高级 - 北桥 - 内存设置 - Memory Remap [开启]



高级 - PCH 存储设置 - SATA 模式选择 [AHCI]



高级 - 高级电源管理(APM) - Erp 支持 [关闭]

高级 - 高级电源管理(APM) - 断电后恢复电源状态 [电源关闭]

高级 - 高级电源管理(APM) - 由 RTC 唤醒 [关闭]

### 启动

启动 - 快速启动 [开启] -> [关闭] 不关貌似没事？

启动 - 安全启动菜单 - 操作系统类型  [其他操作系统]

启动 - CSM (兼容性支持模块) - 开启 CSM [关闭] -> [开启]

启动 - 启动设置 - 开机自检 (POST) 延迟时间 [3秒] -> [2秒]







