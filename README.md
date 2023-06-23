# Arcadyan/Astoria Easybox 904xDSL (VGV952CJW33-E-IR)
[![Openwrt](https://img.shields.io/badge/os-OpenWrt-<COLOR>.svg)](https://github.com/zuzia-dev/openwrt/) [![GitHub release (latest by date)](https://img.shields.io/github/v/release/zuzia-dev/Easybox-904xDSL-repo-source?color=orange)](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/releases/latest) [![GitHub Downloads](https://img.shields.io/github/downloads/zuzia-dev/Easybox-904xDSL-repo-source/total)](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/releases/latest) [![GitHub issues](https://img.shields.io/github/issues/zuzia-dev/Easybox-904xDSL-repo-source?color=green)](https://GitHub.com/zuzia-dev/Easybox-904xDSL-repo-source/issues) ![GitHub latest commit](https://img.shields.io/github/last-commit/zuzia-dev/Easybox-904xDSL-repo-source?color=00BFFF) [![GitHub forks](https://img.shields.io/github/forks/zuzia-dev/Easybox-904xDSL-repo-source?color=93917C)](https://GitHub.com/zuzia-dev/Easybox-904xDSL-repo-source/forks) [![License: GPL v2](https://img.shields.io/badge/License-GPL_v2-blue.svg)](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source#license) 

#### OpenWrt 21.02 with kernel 5.4.x. for Easybox 904 xDSL (VGV952CJW33-E-IR)
<img src="https://raw.githubusercontent.com/zuzia-dev/Easybox-904xDSL-repo-source/79584a2a9e10879312ad694ad44f48ac8a28c6d2/Firmware/Luci-terminal-sysinfo%20v3.jpg" width="512" />

##### [->Images are available in different versions - depending on the type of WAN connection]( https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/releases/tag/v3.OpenWrt)
- SMP - available CPU with two cores
- VPE - FXS port support for VoIP-GSM

- ######  Features included 
Online package repository via Github, LCD and touch keys, printers (p910nd), support for various file systems to enable most drives: ext2/3/4, FAT, F2FS, NTFS, USB storage automounting, Wake-on-LAN (WOL), Point to Point Tunneling Protocol (PPTP), drivers and configuriation for 3G-LTE modems and USB tethering, support for pseudo bridges (relayd), LuCI with HTTPS SSL support and internationalization (en, de, pl), CPU utilization info & Internet detector, script Sysinfo and CPU temperature applet for LuCI (by Cezary Jackiewicz), Terminal integration in LuCI (luci-app-ttyd) and many more.

- ###### Software
Adblock, DDNS (scripts-noip), 3GInfo, Disk Man, Disk Info, Dnsmasq (full), Htop, IP-full, Midnight Commander (mc has mouse support), Nlbwmon, Odhcpd, OpenSSL (and ca-bundle, ca-certificates), OpenVPN, Parted, Picocom, Smartmontools, SMS-Tool, Sudo, Whois, Wireguard, Tc-full, Tcpdump, Timecontrol and many more.

List of useful commands: http://192.168.1.1/cgi-bin/luci/admin/system/commands

#### Perform the following procedures to upgrade the firmware
`Notice: It's recommended to update the bootloader before uploading OpenWrt. Instructions for updating:` [Link](https://openwrt.org/toh/astoria/arcadyan_astoria_easybox_904xdsl_r01#installing_hacked_bootloader)
- ###### Method 1 - via the LuCI graphical web interface
Go to the router’s web interface at http://192.168.1.1 and login. Navigate to LuCI → System → Backup / Flash Firmware → Actions: Flash new firmware image
> Important! Uncheck "Keep settings and retain the current configuration".
- ###### Method 2 - via SSH command line
Open a terminal console on your PC and run ssh root@192.168.1.1 and respond to any prompts regarding fingerprints or passwords. Run the rest of these instructions in the shell you have just logged into on the router.

For SMP version:
```
cd /tmp
wget https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/releases/download/v3.OpenWrt/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-smp-squashfs-sysupgrade.bin
sysupgrade -n -F openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-smp-squashfs-sysupgrade.bin
```
For VPE version:
```
cd /tmp
wget https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/releases/download/v3.OpenWrt/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-vpe-squashfs-sysupgrade.bin
sysupgrade -n -F openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-vpe-squashfs-sysupgrade.bin
```
> WARNING: do not turn off the router until the upgrade finishes!
- ###### Method 3 - via Recovery mode
Follow the instruction: https://github.com/zuzia-dev/Easybox-904xDSL#how-to-use-the-openwrt-recovery-system

### Notes
- ###### Wireless
 WLAN works in AP mode only. Wi-Fi is active, WPA2+AES is set as encryption.
- Network 5 GHz - SSID: EasyBOX-5GHz
- Network 2.4 GHz - SSID: EasyBOX-2GHz
- Default password: WiFipassword
> NOTICE: Do not use LuCI for wireless configuration! Change the default SSID, password or channel number using Terminal.
```
mcedit /etc/config/wireless
```
This option allows you to access to terminal from LuCI web interface: http://192.168.1.1/cgi-bin/luci/admin/services/ttyd

<img src="https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/blob/main/Firmware/Luci-terminal-mode-edit-wireless.jpg?raw=true" width="512"/>

### License
OpenWrt is licensed under GPL-2.0
- The sources are here: https://github.com/OpenWrt-Repository/openwrt
- Compressed (zipped) folders: https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/tree/main/Source
> It based on https://github.com/Plonkbong/openwrt/tree/xrx200-21.02.2
