# Hackintosh

机器配置如下：

主板：微星 MPG Z390 GAMING PRO CARBON

CPU：Intel i7-9700K

内存：金士顿 RGB 8Gx4 3200 灯条

显卡：蓝宝石 RX 570 4G 白金

固态：1.三星960Pro 512G（Mac OS）2.三星SM961 256G（windows 10）

板载声卡：ALC S1220A

板载有线网卡：Intel I219V7

无线蓝牙网卡：Broadcom 94360CD

显示器：LG 27UD68 4K显示器

安装要点：

1.drivers64UEFI里面只能用OsxAptioFixDrv-64.efi，不能用高于V2版本的，这是Z390主板的通病。

2.SMBIOS机型随意，我选择的是iMac Pro。

3.由于Z390不支持原生NVRAM，请添加EmuVariableUefi-64.efi来模拟NVRAM。

4.双系统引导者最好不要在windows下安装Realtek的专有驱动，建议直接使用windows自带驱动，否则出现从windows重启到mac后，alc s1220a声卡声音很小或者无声。

5.关于USB的问题，大部分人都是用遮盖方法来保证端口不大于15个，（ssdt方法，intel-fb-patcher做遮盖kext等），我不喜欢，我要所有usb端口可用，于是用10.14的驱动替换10.14.2的，然后用patch。

正常工作：

显卡：vega 64免驱

有线网卡IntelMausiEthernet.kext驱动

板载声卡：ALC S1220A 用AppleALC.kext驱动

无线蓝牙：94360cd免驱

独立声卡：ESI官方有Mac驱动

睡眠唤醒：正常

开机声音：自行修改加入Duang音效

显卡硬解：正常
