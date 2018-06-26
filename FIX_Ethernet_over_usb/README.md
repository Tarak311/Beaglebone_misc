How to Fix Ethernet over USB (SSH over usb)

1) run sudo ifconfig
 	It will show number of interfaces but ethxxxxxxxxxx won't be there 
2) If it shows up in ifconfig -a
	If there isn't any ip address specified but only mac address then that means no ip address is given by dhcp in your host
3) type $sudo nano /etc/network/interface
	And add follwing lines
	
	auto ethxxxxxx(name from $(ifconfig -a))	
	iface ethxxxxx inet dhcp 

4) restart network service
	sudo service networking restart


