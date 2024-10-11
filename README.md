## JINGYUE B760I SNOW DREAM Hackintosh OpenCore EFI

![image](ScreenShot/JINGYUEB760I.png)

### [简体中文](README.zh_CN.md)

### OpenCore

[OpenCore 1.0.2](https://github.com/acidanthera/OpenCorePkg)

### OS Version Tested

- macOS Monterey 12.x
- macOS Ventura  13.x
- macOS Sonoma   14.x

### Hardware

- Motherboard: B760
- Bios Version: JYI76009 06/06/2023
- CPU: Intel 13th i5-13400
- RAM: KingBank 32GB DDR4 3600Mhz
- SSD: Fanxiang S790 1TB Windows
- SSD: WD SN 770 1TB MacOS
- iGPU: Intel UHD Graphic 730 (Only work in Windows)
- GPU: Sapphire Radeon RX 570 8GB GDDR5
- Audio: Realtek ALC897
- Ethernet Card: Realtek RTL8125 Gaming 2.5GbE
- Ethernet Card: Realtek RTL8168H/8111H
- WIFI: BCM943602CS
- CASE: PCCOOLER Humming Bird i100 PRO
- PSU:  FSP MS 500W 80 BRONZE

### Notes

 - Use [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) or [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) build your SMBIOS
 - If you want to use a CPU without  Efficient-Core, you must uncheck the option in the config.plist file Kernel--ProvideCurrentCpuinfo
 - Intel WiFi driver [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) in this EFI is only applicable to MacOS 14 Sonoma. Please download and replace this driver yourself when installing other MacOS versions
 - Intel Not Supported  Airdrop

### Bios Setup

```
Advanced
  |-- CPU Configuration
     |-- CPU Lock Configuration
	      |-- CFG Lock ：Disabled
	      
	Re-Size BAR Support：Disabled
           
  |-- CSM Configuration
     |-- CSM Support ：Disabled

BOOT
   |-- Secure Boot
      |-- Secure Boot ：Disabled 
```

### Contact Us

QQ Group: 23304408

![image](ScreenShot/QRCode.png)


### Tools

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) AKA `OCAT`.
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA `OCC`.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.
