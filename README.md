# OpenWrt and software repositories for the Arcadyan/Astoria Easybox 904 xDSL

#### OpenWrt 21.02  with kernel 5.4.x. for Easybox 904 xDSL (VGV952CJW33-E-IR)

Available in two versions: 
- [SMP full image](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Firmware/SMP/v1/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-smp-squashfs-sysupgrade.bin) - support 2 cores CPU
- [VPE full image](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Firmware/VPE/v1/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-vpe-squashfs-sysupgrade.bin) - FXS port support for VoIP-GSM 

Support: LCD, touchkeys, 3G-LTE modems, printers, file system ext4, exfat, vfat, msdos, f2fs, ntfs. Software: Adblock, DDNS, LuCI with internationalization and localization (en, de, pl), 3GInfo, Disk Man, Disk Info, Htop, Midnight Commander (mc has mouse support), Nlbwmon, OpenSSL, OpenVPN, Parted, Picocom, Smartmontools, Sysinfo, SMS-Tool, Whois, Wireguard, WOL, Tcpdump, Timecontrol.
List of useful commands: http://192.168.1.1/cgi-bin/luci/admin/system/commands

> Perform the following procedures to upgrade the firmware: 
> 
https://openwrt.org/toh/astoria/arcadyan_astoria_easybox_904xdsl_r01#installing_openwrt_2102_the_easy_way
https://github.com/zuzia-dev/Easybox-904xDSL#small-recovery-with-gui-for-the-easybox-904-xdsl

Wi-Fi is active, WPA2+AES is set as encryption.
- Network 5 GHz - SSID: EasyBOX-5GHz
- Network 2.4 GHz - SSID: EasyBOX-2GHz
- Default password: WiFipassword
> NOTICE: Do not use LuCI for wireless configuration! All Wi-Fi settings must be made in the command line with vi or mcedit.

### License
OpenWrt is licensed under GPL-2.0
