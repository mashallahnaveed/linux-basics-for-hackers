📘 Chapter 3: Analyzing and Managing Networks

🧠 Overview

This chapter introduces essential Linux networking commands used to analyze, configure, and manipulate network settings. These skills are fundamental for cybersecurity and ethical hacking.

🌐 Viewing Network Information

🔹 ifconfig

Displays network interface details (IP address, MAC address, etc.)

ifconfig

Shows all active network interfaces

Useful for checking IP address

🔹 iwconfig

Displays wireless network interfaces

iwconfig

Used for Wi-Fi interfaces

Shows SSID, mode, frequency

🔧 Changing Network Information

🔹 Change IP Address

ifconfig eth0 192.168.1.10

Assigns a new IP address to interface

🔹 Change Network Mask

ifconfig eth0 netmask 255.255.255.0

🔹 Change Broadcast Address

ifconfig eth0 broadcast 192.168.1.255

🔹 Assign IP via DHCP

dhclient eth0

Gets IP automatically from DHCP server

🕵️ MAC Address Spoofing

🔹 Change MAC Address

ifconfig eth0 down

ifconfig eth0 hw ether 00:11:22:33:44:55

ifconfig eth0 up

Changes hardware (MAC) address

Used for anonymity

🌍 Domain Name System (DNS)

🔹 dig

Used to query DNS information

dig google.com

Returns IP address and DNS details

🔹 Change DNS Server

Edit the resolv.conf file:

nano /etc/resolv.conf

Example:

nameserver 8.8.8.8

🔹 Map IP Addresses Manually

Edit hosts file:

nano /etc/hosts

Example:

127.0.0.1   localhost

192.168.1.5 testsite.com

🧪 Practical Examples

ifconfig

👉 Check your current IP address

ping google.com

👉 Test internet connectivity

dig example.com

👉 Get DNS details

🧠 Key Takeaways

Learned how to analyze network interfaces

Understood IP address configuration

Practiced MAC address spoofing

Learned DNS manipulation techniques

⚡ Quick Summary

Command	                 Description

ifconfig	               Show network info

iwconfig	               Wireless info

dhclient	               Get IP from DHCP

dig	                      DNS lookup

/etc/resolv.conf	DNS config

/etc/hosts	Local domain mapping

🚀 Notes

Network commands often require root privileges

Misconfiguration can break connectivity

Always verify changes after applying

