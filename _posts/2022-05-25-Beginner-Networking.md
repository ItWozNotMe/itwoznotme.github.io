Type: #TryHackMe <br>
Links: https://tryhackme.com/room/whatisnetworking <br>
Topics: #Networking <br>

## Identifying Devices on a Network

Devices has two means of identifications, these are :

An IP ADDRESS
A MEDIA CONTROL ACCESS (MAC) ADDRESS
Trash/Misc 1/Images/Pasted image 20210831142325.png

An IP Address is a set of numbers that are divided into four octets, this number is calculated through Subnetting. IP Addresses can change from device to device but two devices cannot share the same IP Address.

A public address is used to identify a device on the Internet , whereas a private address is used to identify a device amongst over devices

![image](https://user-images.githubusercontent.com/74746341/170378063-5ad233d1-0ae6-4dfc-9ea6-3f5e3db79f7d.png)

The two private devices will use their private IP to communicate with each other, but any data sent over the internet from eaither device will be identified by their public IP address.

IPv4 is limited in as their is only 2^32 IP addresses (4.29 billion)

IPv6 Aims to solve this issue as it supports 2^128 (340 trillion-plus) IP addresses and is more efficient due to new methodolgies.

![image](https://user-images.githubusercontent.com/74746341/170378145-832f19ba-f52b-476f-8102-00ac4d3be3f9.png)

## Mac Addresses

Devices on a network will all have a physical network interface, which is a microchip board found on the device's motherboard. This is assigned a unique address of a twelve-character hexadeimal number.

Example MAC : a4:c3:f0:85:ac:2d

The first six characters represent the comapny that made the interface and the last six is a unique number

MAC Addresses can be faked or "spoofed" PythonMACScript in a process know as spoofing.

Places such as cafes, coffee shops, and hotels alike often use MAC address control when using their "Guest "or "Public" Wi-Fi. This configuration could offer better services, i.e. a faster connection for a price if you are willing to pay the fee per device.

![image](https://user-images.githubusercontent.com/74746341/170378371-07274957-a630-4d5e-b2cb-81884419768c.png)

## Ping

Ping is a network tool that uses Internet Control Messege Protocol (ICMP) packets to determine the connection between devices. Pings can be performed against devices on a network. The syntax is:

ping "ip address or website url"

 
