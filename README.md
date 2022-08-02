# OpenWrt and software repositories for the Arcadyan/Astoria Easybox 904 xDSL

#### OpenWrt 21.02  with kernel 5.4.x. for Easybox 904 xDSL (VGV952CJW33-E-IR)

Available in two versions: 
- [SMP full image](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Firmware/SMP/v1/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-smp-squashfs-sysupgrade.bin) - available CPU with two cores
- [VPE full image](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Firmware/VPE/v1/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-vpe-squashfs-sysupgrade.bin) - FXS port support for VoIP-GSM 

- ######  Features included 
LCD and touch keys, printers (p910nd), support for various file systems to enable most drives: ext2/3/4, FAT, F2FS, NTFS, USB storage automounting, Wake-on-LAN (WOL), Point to Point Tunneling Protocol (PPTP), drivers and configuriation for 3G-LTE modems and USB tethering, support for pseudo bridges (relayd), LuCI with HTTPS SSL support and internationalization (en, de, pl), script Sysinfo and CPU temperature applet for LuCI (by Cezary Jackiewicz). 

- ###### Software
Adblock, DDNS (scripts-noip), 3GInfo, Disk Man, Disk Info, Dnsmasq (full), Htop, IP-full, Midnight Commander (mc has mouse support), Nlbwmon, Odhcpd, OpenSSL (and ca-bundle, ca-certificates), OpenVPN, Parted, Picocom, Smartmontools, SMS-Tool, Sudo, Whois, Wireguard, Tc-full, Tcpdump, Timecontrol. 

List of useful commands: http://192.168.1.1/cgi-bin/luci/admin/system/commands

#### Perform the following procedures to upgrade the firmware
- ###### Method 1 - via the LuCI graphical web interface
Go to the router’s web interface at http://192.168.1.1 and login. Navigate to LuCI → System → Backup / Flash Firmware → Actions: Flash new firmware image
> NOTICE:  Untick [Keep Settings](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/blob/8206ebac1623019f21bff2e18c7ca9ce6ab2c9bd/Firmware/Upgrade_via_LuCI.jpg?raw=true)
- ###### Method 2 - via SSH command line
Open a terminal console on your PC and run ssh root@192.168.1.1 and respond to any prompts regarding fingerprints or passwords. Run the rest of these instructions in the shell you have just logged into on the router.

For VPE version:
```
cd /tmp
wget https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Firmware/VPE/v1/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-vpe-squashfs-sysupgrade.bin
sysupgrade -n -F openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-vpe-squashfs-sysupgrade.bin
```
For SMP version:
```
cd /tmp
wget https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Firmware/SMP/v1/openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-smp-squashfs-sysupgrade.bin
sysupgrade -n -F openwrt-lantiq-xrx200-arcadyan_vgv952cjw33-e-ir-smp-squashfs-sysupgrade.bin
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
> NOTICE: Do not use LuCI for wireless configuration! All Wi-Fi settings must be made in the command line with vi or mcedit.

### License
OpenWrt is licensed under GPL-2.0

The source are here: [Easybox-904xDSL-source-openwrt-21.02-v1.zip](https://github.com/zuzia-dev/Easybox-904xDSL-repo-source/raw/main/Source/Easybox-904xDSL-source-openwrt-21.02-v1.zip) 
It based on [Plonkbong`s source](https://github.com/Plonkbong/openwrt/tree/xrx200-3)
