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

After completing the installation wizard and a quick install the next stage was to self-sign the website preventing man-in-the-middle attacks.





