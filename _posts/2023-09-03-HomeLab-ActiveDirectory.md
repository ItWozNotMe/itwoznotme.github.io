## Home Lab Active Directory Setup

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d19535ee-642f-4080-8e33-f8929b9eea91)


Type: #Homelab <br>
Software: Oracle VM VirtualBox Manager

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/957b603f-cfe4-46b4-bf57-bc7a47b2b9de)

This walkthrough involves setting up and configuring the active directory on Microsoft Windows Server 2019, using
Oracle VM VirtualBox Manager as the virtualization software. Download links are available here:

https://www.virtualbox.org/wiki/Download_Old_Builds_6_1 <br>
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

Next, the DC virtual machine needs to be re-launched. Installing active directory can be done via the server manager.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/e8fd36b4-eaa1-4fb2-bcf4-f389a5793581)

Following the installation wizard, within the results section a new forest can be created; a forest is a logical container that contains the domains, users, computers and group policies. This can be done after promoting the server to a domain controller

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/aca52a81-f574-4f9e-9723-1da4c89fd266)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/3510d995-3784-42b6-a6c3-25c75b098a9c)

Following the installation wizard, and waiting for the installation, after a restart the domain controller was successfully installed.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/ff51285e-324b-42cf-923d-3b28fc335cc5)

The next stage is to create a new user, I created a helpdesk account, and will then allocate it some permissions.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/40dc16ba-72ae-4cea-99c7-c7076ad57b63)

Clicking properties on the helpdesk account and navigating to "member of" I allocated the helpdesk the domain admin role.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/6354f3cb-10a7-40cd-9d57-b933b0d9fdfe)

Launching the helpdesk virtual machine, the domain controller IP address can be set as the helpdesk's DNS server.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/70429ca3-1b3c-422f-88c0-71c2d7489da2)

After this the domain name can be entered through access work or school, followed by entering the credentials established by the dc.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/c76a1477-8e0b-4415-b68f-cd79955f2713)

Navigating to the domain controller, under the management for active directory > computers the helpdesk virtual machine can be seen, confirming their connection.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/fb7f51c4-888a-478d-869f-ec8edd96d3ef)

The staff machine will not be configured due to hardware limitations; the next steps for understanding would be:

https://tryhackme.com/room/activedirectoryhardening <br>
https://tryhackme.com/room/adenumeration <br>
https://tryhackme.com/room/exploitingad <br>





