# image notes
sudo make UNAME=bartendro UPASS=boozey RPASS=rootboozey

### packages needed
git
python3.6
hostapd
dnsmasq
iptables
dhcpcd5
bridge-utils

/etc/network/interfaces.d/*.cfg
create wlan1.cfg

sudo nano /etc/dhcpcd.conf

interface wlan0
static ip_address=192.168.0.10/24
denyinterfaces eth0
denyinterfaces wlan0

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

### setting up wifi host
https://thepi.io/how-to-use-your-raspberry-pi-as-a-wireless-access-point/
https://frillip.com/using-your-raspberry-pi-3-as-a-wifi-access-point-with-hostapd/
install hostapd dnsmasq
edit config files
sudo service hostapd start
sudo service dnsmasq start
sudo /etc/init.d/networking restart
