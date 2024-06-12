## Homelab Networking

This project involves physical networking; having purchased a switch and using an older PC to create a firewall and IPS/IDS I intend to configure my home network. The majority of the network cannot be configured. It will therefore be ignored with the focus on my network segment following the router to my firewall and then outward into the switch and local area network. This project aims to learn about physical networking and configure subnets and VLANS, ending with configuring opensense as a firewall and IPS/IDS. 


![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/96fcd3f6-8329-4940-b914-aec82ef451cf)


| Assets              | IP Address | Domain| Phyiscal Location |
|--------------------|------------|-------|-------------------|
| HP Prodesk (Firewall) | 10.10.42.1 | LAN/WAN | Home         |
| Switch             |10.10.42.20 | Local | Home              |
| Raspberry Pi       |10.10.42.21 | Local | Home              |
| Personal PC        |10.10.42.22 | Local | Home              |
| Google Pixel 6     | Mobile 4G  |External| Home & External  |

## Intended Networking Features/Security Implementations

As this is a bigger project I intend to include multiple security features for networking, allowing for several learning opportunities and a chance to use some enterprise equipment and features at home including:

- Network Segmentation
VLANS: This will be achieved by the Netgear GS305E allowing for VLAN support via its management interface. The benefits of this include a trusted LAN for main devices such as the Raspberry Pi and my PC and an IoT VLAN for phones and IoT devices. VLANS are a logical way of separating a group of devices into a networking group, resulting in a series of benefits such as improved security, resource management and improved network perform.  
- Firewall Configuration
A firewall will be configured using opensense to achieve INTER-VLAN traffic control, port forwarding and filtering based on MAC addresses. A firewall is a network security device that can block incoming and outgoing traffic based on a series of rules.
- Access Control
The server will only be accessible outside the network via a VPN, currently, tailsacle is used, this might be replaced by OpenVPN as it is completely self-hosted with no dependency on a third-party company.
- DNS Security
A DNS server will be configured via proxmox on the HP Prodesk or containerized on the Raspberry Pi. Pi-hole was the intended solution as it is lightweight and allows for ad-blocking and the ability to block
malicious domains via a blacklist, additionally allowing for DNS over HTTPS.
- Website Security
The final solution will involve self-hosting a website on a new lightweight device on a separate VLAN or subnet to minimize the impact of a compromise.

## Firewall Setup

Initially, I planned to set up proxmox on the HP Prodesk and virtualise opensense using a type 1 hypervisor, I tested this configuration on a laptop and decided to run it on a dedicated machine ensuring better performance. Proxmox can be avoided as its main goal was to install opensense on one virtual machine and a DNS server on another. The only requirement of the server is to be accessible outside the network shown in the initial diagram; only VLAN2 needs to be accessible. This could be achieved by MAC filtering or other firewall rules and will be configured upon installation and the initial setup of opensense. 

Opensense was booted onto the HP Prodesk using balenaEtcher and configuring the boot from USB option in the bios, following an easy installation selecting my LAN and WAN interfaces and then navigating to my firewall within the browser. 

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/e412a704-6195-487a-bbf5-c1b7c9749066)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/16e4e375-a785-4f6e-80de-50a53abb93d1)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d5eb58d2-12ab-41e3-956a-187279e531fa)

## Setting Up First Rules

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d60187c9-b034-4f83-807b-14aa4033366c)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/a2e84065-1272-49bd-aa3a-3dc5fe15fe48)


My first rule was to block incoming traffic from a telnet port left open by another user. I also blocked this for LAN users as I intend to use SSH as a more secure alternative.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/aff470f0-51d5-47b9-b590-358e8f64c495)

## Explanation of Rules

Incoming Telnet Traffic: The first rule blocks Telnet traffic coming from the internet into your network. This prevents external entities from initiating Telnet connections to devices within your network.

Outgoing Telnet Traffic: The second rule blocks Telnet traffic originating from devices within your network and attempting to connect to external Telnet servers. This prevents devices within your network from using Telnet to connect to potentially insecure external services.

These same rules were applied to rcpbind

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/0e779bd7-b176-4cf5-bdad-89b56596a2f4)
![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/17fe249c-17ed-449f-b6d2-58db1f319455)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/0e3262e8-fc7a-4310-9eea-7141bb78bced)
![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/9199c079-ac2a-406f-b9fa-d1dc6396f8b9)

These screenshots show an attempt to connect to ports 111 and 22 that were blocked on Opnsense resulting in the connection being refused meaning the firewall is working as intended.


## Future Improvements (Part Two)
1. My main PC now has wifi up and running but cannot ping 192.168.0.105 (Raspberry Pi) as it is not in the same subnet, this would need to be configured by turning DHCP on within the network config file.
2. Pi-Hole on Raspberry Pi
3. PKI and Self-Signed Certificates for Opnsense and other self-hosted sites.



