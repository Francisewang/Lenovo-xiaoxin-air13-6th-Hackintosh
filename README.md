# Lenovo-xiaoxin-air13-6th-Hackintosh
联想小新Air 13（i5 6200U/8GB/256GB）无独显版本
# 一、机型配置
| 硬件  | 型号  |
| ------------ | ------------ |
| 处理器名称  |Intel 酷睿i5 6200U |
|  	主板名称  |	联想小新Air 13（i5 6200U/8GB/256GB）|
| 系统内存  |  	8192MB (DDR3 SDRAM 1866mhz) |
|  显示适配器 |   Intel(R) HD Graphics 520 (1 GB)|
| 	显示器    |  	[13.3" LCD]1080P |
| 音频适配器   | 	Realtek ALC236  |
|  硬盘 | 	三星nvme (256 GB)  |
|  WiFi 蓝牙 |	bcm94352hmz 自行更换，无白名单|
|  BIOS版本 |	0ncn42ww|
# 二、安装之前BIOS设置
	-bios中将raid硬盘模式切换为ahci
	-Disabled Secure Boot  
	-uefi only →legancy support
# 三、运行状态
## 正常运行列表
	显卡HD520驱动正常，注入ID 0x19160000  
	声卡ALC236驱动正常，注入ID 11  
	键盘触摸板正常，均为PS2设备  
	usb正常，usbinjectall.kext+ssdt_uiac.aml定制  
	HDMI输出正常  
	睡眠唤醒正常  
	原生电源管理  
	亮度调节  
	wifi蓝牙正常  
	iMessage、FaceTime、iCloud、airdrop正常  
	系统可随意升级，注意更新clover版本跟驱动版本  
## 不正常运行列表
	sd读卡器  
# 四、DSDT补丁
## 对DSDT打下列补丁  
	Fix system_HPET  
	Fix system_IMEI  
	Fix system_IRQ  
	sys system_OSYS_win10  
	Fix system_WAK Arg0 V2  
	Fix system_RTC 
	Fix system_SMBUS  
	Fix system_PNOT/PPNT  
	Fix usb_prw_0x6d_xhc  
	Fix Mutex with non-zero synclevel  

## 四、备注
	 内存报错需要在smbios添加内存信息才能成功进入clover界面安装。  
