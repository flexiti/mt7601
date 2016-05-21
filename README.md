# mt7601
Mediatek MT7601 driver (copy of oryginal Mediatek driver Copyright 2002-2010, Ralink Technology, Inc.)

usage:

sudo apt-get install linux-headers-generic build-essential git

sudo apt-get install git

git clone https://github.com/flexiti/mt7601.git 

cd mt7601

make clean 

make

sudo make install

sudo mkdir -p /etc/Wireless/RT2870STA/

sudo cp RT2870STA.dat /etc/Wireless/RT2870STA/

sudo modprobe mt7601Usta

Your wireless should now be working.
Tested on Armbian (Debian Jessy and Ubuntu Trusty)
ps.
network config example:

        auto ra0
	iface ra0 inet static     
        address 192.168.0.2
        netmask 255.255.255.0
        gateway 192.168.0.1 
        wpa-ssid YOURSID
        wpa-psk YOURPASS
        dns-nameservers 8.8.8.8 8.8.4.4 
        
  The original vendor driver can be downloaded from MediaTek's website 
  (http://www.mediatek.com/en/downloads1/downloads/mt7601u-usb/).       
        
