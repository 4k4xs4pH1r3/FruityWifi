# FruityWiFi
###### Wireless network auditing tool http://www.fruitywifi.com/

FruityWiFi is an open source tool to audit wireless networks. It allows the user to deploy advanced attacks by directly using the web interface or by sending messages to it. 

Initialy the application was created to be used with the Raspberry-Pi, but it can be installed on any Debian based system. 

![Status](http://www.fruitywifi.com/img/001.png)

A more flexible control panel. Now it is possible to use FruityWifi combining multiple networks and setups: 

Within the new options on the control panel we can change the AP mode between Hostapd or Airmon-ng allowing to use more chipsets like Realtek. 

It is possible customize each one of the network interfaces which allows the user to keep the current setup or change it completely.

![Config](http://www.fruitywifi.com/img/002.png)

FruityWifi is based on modules making it more flexible. These modules can be installed from the control panel to provide FruityWifi with new functionalities. 

Within the available modules you can find URLsnarf, DNSspoof, Kismet, mdk3, ngrep, nmap, Squid3 y SSLstrip (code injection functionality), Captive Portal, AutoSSH, Meterpreter, Tcpdump and more. 

**Note**: New modules are being developed continuously and can be installed from the modules page.

## For Install in any Debian based Distro

Use this installation script:

### Add Kali Repo to any Debian based Distro

On a standard, clean install of Debian Distro Based Linux, you should have the following entry present in /etc/apt/sources.list:

      nano /etc/apt/sources.list
       
For Parrot Security add here

      nano /etc/apt/sources.list.d/parrot.list
       
deb http://http.kali.org/kali kali-rolling main contrib non-free
deb-src http://http.kali.org/kali kali-rolling main contrib non-free
       
       sudo apt-key adv --recv-keys --keyserver keys.gnupg.net 7D8D0BF6
       

### Integrate Kali with Debian

       apt-get clean && apt-get update && apt-get upgrade && apt-get dist-upgrade && apt-get install python-pil:i386 -y && apt autoremove -y
       
### Instal mitmf & python

      sudo apt-get install python-pip python3-pip python-dev python-setuptools libpcap0.8-dev libnetfilter-queue-dev libssl-dev libjpeg-dev libxml2-dev libxslt1-dev libcapstone3 libcapstone-dev libffi-dev file -y && pip install virtualenvwrapper

#

Edit your .bashrc or .zshrc file to source the virtualenvwrapper.sh script:, adding this line ate the of the file
#
source /usr/local/bin/virtualenvwrapper.sh
#
      cd /root && nano .basrc

The location of this script may vary depending on your Linux distro.
#

Restart your terminal or run:

      source /usr/bin/virtualenvwrapper.sh
      

https://github.com/byt3bl33d3r/MITMf/wiki/Installation


### Install FruityWiFi x86/x64 Version

    apt install neofetch screenfetch -y && cd /usr/share/ && wget https://github.com/xtr4nge/FruityWifi/archive/master.zip && unzip master.zip && neofetch && cd FruityWifi-master && python install-modules.py && screenfetch && ./install-FruityWiFi.sh
    

Go to **http://localhost:8000** (for http) <br>
Go to **https://localhost:8443** (for https) 

user: admin<br>
pass: admin
<br><br>

### Kali Linux Version

**Note**: The Kali Linux version has not been updated in long time. I will try to work on this as soon as I can. For the moment use the GitHub installer for avoiding issues.

FruityWiFi is now part of Kali Linux repositories.
- `apt-get install fruitywifi`
- `/etc/init.d/fruitywifi start`
- `/etc/init.d/php5-fpm start`

Go to **http://localhost:8000** (for http) <br>
Go to **https://localhost:8443** (for https) 

user: admin<br>
pass: admin
<br>

Note: installing `fruitywifi` will install all modules. If you want to install only some modules, you can install  `fruitywifi-core` first and then each module, for example `fruitywifi-module-dnsspoof`. 
<br><br>

### ARM version (Raspberry Pi)

**Note**: The new installer has not been tested on Raspberry yet. I will try to work on this as soon as I can.

- You need a Raspbian, Pwnpi or Kali Linux version to use this script.
- Download the zip file from https://github.com/xtr4nge/FruityWifi/archive/master.zip
- Unzip the file and run **install-FruityWiFi.sh** (This script will install all the dependencies and setups)
- Done. 

Go to **http://localhost:8000** (for http) <br>
Go to **https://localhost:8443** (for https) 

user: admin<br>
pass: admin
<br><br>


### Install and Activate all the modules manually

1. https://localhost:8443/page_modules.php?show-deb

2. https://localhost:8443/page_modules.php?show


### More information
[Wiki](https://github.com/xtr4nge/FruityWifi/wiki)
