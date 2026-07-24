## 精粤 B760I SNOW DREAM 黑苹果 OpenCore EFI

![image](ScreenShot/JINGYUEB760I.png)

### [ENGLISH](https://github.com/hackintosh-club/JINGYUE-B760I-SNOW-DREAM-OpenCore)

### OpenCore

[OpenCore 1.0.7](https://github.com/acidanthera/OpenCorePkg)

### macOS

- macOS Monterey 12.x
- macOS Ventura    13.x
- macOS Sonoma   14.x
- macOS Sequoia   15.x
- macOS Tahoe   26.x

### EFI 主要组件

| 组件 | 版本 / 配置 |
| --- | --- |
| OpenCore | 1.0.7 |
| Lilu | 1.7.3 |
| VirtualSMC | 1.3.8 |
| WhateverGreen | 1.7.1 |
| AppleALC | 1.9.8 |
| RestrictEvents | 1.1.7 |
| RealtekRTL8111 | 2.5.0 |
| LucyRTL8125Ethernet | 1.2.3 |
| USB 定制 | SimpleUSBMap 1.0.2 |
| 博通无线兼容 | AMFIPass 1.4.1、IOSkywalkFamily、IO80211FamilyLegacy |

### 硬件

- 芯片组: B760
- Bios 版本: JYI76009 06/06/2023
- 处理器: 英特尔13代 i5-13400
- 内存: 金百达 银爵 32GB DDR4 3600Mhz
- 硬盘: 梵想 Fanxiang S790 1TB Windows
- 硬盘: 西数 SN 770 1TB MacOS
- 核显: 英特尔超核心显卡730 (仅在Windows中可以使用)
- 独显: 蓝宝石 Radeon RX 570 8GB GDDR5
- 声卡: 瑞昱 ALC897
- 有线网卡:  瑞昱 RTL8125 Gaming 2.5GbE
- 有线网卡: 瑞昱 RTL8168H/8111H
- 无线网卡: BCM943602CS
- 处理器散热：利民 AXP90-AX47
- 机箱:  超频三 蜂鸟 i100pro
- 电源:  全汉经典版 MS 500W 80 铜牌全模组

### BIOS设置

```
高级
     |-- CPU电源管理控制
        |-- CPU锁配置
	         |-- CFG锁定：关闭
	   |-- PCI总线驱动版本     
	       |-- Re-Size BAR Support：Disabled
     |-- CSM配置
	      |-- CSM支持：关闭
		
启动
  |-- 安全启动
    |-- 安全启动：关闭
```

### 注意事项

- 安装成功后，请使用 [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) 生成你自己的 SMBIOS 信息，不要直接沿用 `config.plist` 中的示例身份信息。
- 如需使用没有能效核（小核心）的 CPU，请在 `config.plist` 中关闭 `Kernel -> Quirks -> ProvideCurrentCpuInfo`。
- 当前内置无线配置对应硬件列表中的 BCM943602CS。在 macOS Sonoma 14 及更高版本中，通过 `IOSkywalkFamily.kext`、`IO80211FamilyLegacy.kext` 和 `AMFIPass.kext` 提供兼容，并需要使用 [OpenCore Legacy Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher) 应用相应的根补丁。
- 当前配置为较新 macOS 保留了兼容启动参数 `-lilubetaall`；待相关 Kext 正式支持所用系统版本后，可将其移除。
- USB 定制已改用 `SimpleUSBMap.kext`，不再使用原来的 `USBToolBox.kext` 和 `UTBMap.kext`。

### 参考内容

[1.黑苹果安装过程演示](https://hackintosh.club/d/10000060)

[2.英特尔无线网卡WiFi驱动](https://hackintosh.club/d/10000015)

[3.英特尔无线网卡蓝牙驱动](https://hackintosh.club/d/10000017)

[4.我的B站黑苹果教程](https://space.bilibili.com/244390800/video)

[6.黑果之家](https://hackintosh.club)


### 联系我们

QQ群: 23304408

![image](ScreenShot/QRCode.png)



### 常用工具
- [OpenCore-Legacy-Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher)
- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) AKA `OCAT`.
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA `OCC`.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.
