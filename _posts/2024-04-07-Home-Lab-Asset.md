## Home Lab Asset Creation

This project involves running an linux server, with the aim of it running during the day. The scope of the project is to have an server that can be accessed internally and externally via a webpage or application. To fufil this requirement
a raspberry pi was purchased as my usual projects involve a virtual machine which would have been too costly. Therefore, a rasberry 4 with 8gb of ram was used running ubuntu server on arm archiecture. This project will be broken up into four parts: Installation of ubuntu server, docker and portainer install, installation of assets and final comments, security measures and future implementations.

## Installation of Ubuntu Server
The stock microSD of 32GB was flashed using raspberry pi imager and ubuntu server was selected under other "general purpose operating systems"

![1443a1624b2c3e4f48bc2ec18dbadbdfb052f636_2_690x464](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/f5dca129-a359-41e0-85d4-c292d9ab71bb)

![c480bccc0de84dacd2b2523b398188b39210e3d8_2_690x448](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/07a7b3b2-ec60-464d-ab98-465f02ba9c03)

This installation is very easy and shouldn't take too long, whilst the SD card being flashed ensure that you have a usb to HDMI cable, a usb keyboard and a micro-USB-C cable to power the raspberry pi. After the SD has been flashed insert it into the back of the
raspberry pi and turn it on by plugging in a usb-c cable, the follow the instructions to finish the installation.

![PXL_20240407_191614146](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/dc4dfc22-a489-4084-a0f3-f36e8f3ac0c4)

## Portainer Install

To start installing docker ensure that the system is up to date using "sudo apt-get update && upgrade" after this install docker using "sudo apt insatll docker-ce". The command to install portainer is:

docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest

this command installs portainer on port 9443 and starts the dockerized container on boot, the two commands -v are refrencing the storage place followed by a bind storage on the physical drive.

![tempsnip](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/86f14b85-26ea-486f-9839-bf51f877bdbb)

After creating a secure password on portainer at "https://localhost:9443" navidrome can be deployed via stacks

## Asset One

Navidrome Application port 4533

![tempsnip](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/5f6a9926-cdec-4cc0-8c22-cd646dd13a76)

Music can then be added to the server ONLY if a license is aquired and music is stored legally, genrally in the UK you are allowed one digital copy and can only use it if the content is not shared or sold for profit. I am not uploading music to the server as this is project is more about creating assets that I will secure and defend with the intention of creating asset management reports to develop skills within cyber security whilst also learning ubuntu server. 

## Asset Two 

Generic SSH Configuration

## Asset Three

Server Home Screen


The creation of three assets with defualt configurations allows for me to test these apps and services via a asset management report and a penetration test, developing my writing and skills within security. The setup also helps my general IT skills by managing a server.
