## Home Lab Active Directory Setup

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/957b603f-cfe4-46b4-bf57-bc7a47b2b9de)

This walkthrough involves setting up and configuring the active directory on Microsoft Windows Server 2019, using
Oracle VM VirtualBox Manager as the virtualization software. Download links are available here:

https://www.virtualbox.org/wiki/Download_Old_Builds_6_1
https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/302b499d-65ae-492f-a554-5b3bd65aa7d5)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/620dc27d-6b05-470c-b033-c9de6179f6bf)

Before starting the installation I configured the settings of the Windows server, changing the network adapter to 
bridged and removed the floppy disk from the boot order. This allows the machine to be booted from the ISO.


![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/dfbda2ca-3196-4638-8e04-a344e01e8b84)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/9ae3959e-e345-4ed9-a381-c8c875f3216f)

After this, a custom install was selected. This will install a clean operating system and will be used as the
domain controller for my virtual server.

Upon Installation the name will need to be changed to DC this can be done via Settings.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/74c66fc0-e35a-4050-8fa7-f49218b73a73)

After this a client machine will need to be set up, this can be done by installing the Windows 10 enterprise edition from https://www.microsoft.com/en-gb/evalcenter/download-windows-10-enterprise and selecting 64-bit download. This machine has the same settings as the server, using a bridged network and removing the floppy disk. The machine is called the helpdesk to replicate a real scenario. This machine will need to have its name changed to helpdesk in the settings, and then cloned, creating a new machine called staff.
