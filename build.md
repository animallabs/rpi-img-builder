# image notes
sudo make UNAME=bartendro UPASS=boozey RPASS=rootboozey

### packages needed
git
python3.6

/etc/network/interfaces.d/*.cfg
create wlan1.cfg


### add network for wlan0
/etc/wpa_supplicant/wpa_supplicant.conf
network={
	ssid="The Port Mall"
	psk="Th3P0rt317"
}

### get wifi dongle to work
/etc/apt/sources.list
deb http://http.debian.net/debian/ stretch main contrib non-free
apt-get install firmware-misc-nonfree

### to look into
i2c
spi
gpio
