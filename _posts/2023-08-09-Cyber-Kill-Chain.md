## Cyber Kill Chain

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/b250cc51-2ee7-4f01-9fcd-01203fcb18c1)

Type: #TryHackMe <br>
Links: https://tryhackme.com/room/cyberkillchainzmt <br>

This is a walkthrough for TryHackMe's Cyber Kill Chain room under the SOC Level 1 learning path.

Learning Objectives: In this room, you will learn about each phase of the Cyber Kill Chain Framework and the advantages and disadvantages of the traditional Cyber Kill Chain. 

## Introduction
The cyber kill chain is a framework based on the military concept "kill chain", introduced in 2011 consisting of seven stages: reconnaissance, weaponization, delivery, exploration, installation, command & control
and actions & objectives. The objective of the cyber kill chain is to assess the network and system security by identifying missing security controls and filling these missing gaps.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/51144e92-0afd-4366-a264-c122ccb268eb)

## Reconnaissance

Reconnaissance is the process of discovering and collecting information on the system and the victim, OSINT (Open-Source Intelligence) also falls under this, typically involving the planning phase by collecting
every available piece of information e.g. company, employee names/email addresses and phone numbers. This room looks at email harvesting more in-depth than other OSINT methods, defining it as: <br>

'Email harvesting is the process of obtaining email addresses from public, paid, or free services. An attacker can use email address harvesting for a phishing attack 
(a type of social-engineering attack used to steal sensitive data, including login credentials and credit card numbers). ' <br>

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/51631700-947d-4da0-bb84-2bc1a29e0200)

## Weaponization

Upon completion of a successful reconnaissance stage, the threat group would create a "weapon", this could be a combination of malware and an exploit into a deliverable payload.

Definitions

Malware is a program or software that is designed to damage, disrupt, or gain unauthorized access to a computer.

An exploit is a program or code that takes advantage of the vulnerability or flaw in the application or system.

A payload is a malicious code that the attacker runs on the system.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/34be39b3-336f-4f9c-8e0d-706c5dc332ee)

## Delivery

This stage involves choosing a method for transmission of the payload/malware. TryHackMe provides three methods alongside a definition: 

Phishing email: after conducting the reconnaissance and determining the targets for the attack, the malicious actor would craft a malicious email that would target either a specific person 
(spearphishing attack) or multiple people in the company. The email would contain a payload or malware. 

Distributing infected USB drives in public places like coffee shops, parking lots, or on the street. An attacker might decide to conduct a sophisticated USB Drop Attack by printing the company's 
logo on the USB drives and mailing them to the company while pretending to be a customer sending the USB devices as a gift. You can read about one of these similar attacks at CSO Online "Cybercriminal group mails malicious USB dongles to targeted companies."

Watering hole attack. A watering hole attack is a targeted attack designed to aim at a specific group of people by compromising the website they are usually visiting and then 
redirecting them to the malicious website of an attacker's choice. The attacker would look for a known vulnerability in the website and try to exploit it.
The attacker would encourage the victims to visit the website by sending "harmless" emails pointing out the malicious URL to make the attack work more efficiently. After visiting the website, 
the victim would unintentionally download malware or a malicious application to their computer. This type of attack is called a drive-by download. An example can be a malicious pop-up asking to download a fake
Browser extension.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/216c734a-274a-437d-ad5b-6fe013f255ed)

## Explotation

Exploitation involves the successful infiltration of a system, after gaining this access the malicious actor would likely further exploit the software, system or server to escalate privileges or move 
through the network. "lateral movement refers to the techniques that a malicious actor uses after gaining initial access to the victim's machine to move deeper into a network to obtain sensitive data." 

These are examples of how an attacker carries out exploitation:

    The victim triggers the exploit by opening the email attachment or clicking on a malicious link.
    Using a zero-day exploit.
    Exploit software, hardware, or even human vulnerabilities. 
    An attacker triggers the exploit for server-based vulnerabilities. 

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/365b8e5e-4371-4261-bd1c-4dfa133bbee7)

## Installation 

Upon successful exploitation a method of persistence such as a backdoor or an access point. TryHackMe concludes that persistence can be achieved through:

Installing a web shell on the webserver. A web shell is a malicious script written in web development programming languages such as ASP, PHP, or JSP used by an attacker to maintain access to the compromised system. 
Creating or modifying Windows services. This technique is known as T1543.003 on MITRE ATT&CK (MITRE ATT&CK® is a knowledge base of adversary tactics and techniques based on real-world scenarios). An attacker can create or modify the Windows services to execute the malicious scripts or payloads regularly as a part of the persistence. An attacker can use the tools like sc.exe (sc.exe lets you Create, Start, Stop, Query, or Delete any Windows Service) and Reg to modify service configurations. The attacker can also masquerade the malicious payload by using a service name that is known to be related to the Operating System or legitimate software.
Adding the entry to the "run keys" for the malicious payload in the Registry or the Startup Folder. By doing that, the payload will execute each time the user logs in to the computer. According to MITRE ATT&CK, there is a startup folder location for individual user accounts and a system-wide startup folder that will be checked no matter what user account logs in.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/0014e7eb-76dd-4f7f-9d00-01e5afe36e46)

## Command & Control

After maintaining persistence and executing malware on the target machine, a C2 (Command and Control) channel can be opened to remotely control the victim. This is known as C&C or C2 Beaconing establishing communication between the C&C server and the infected host. The most common C2 channels used by adversaries nowadays:

    The protocols HTTP on port 80 and HTTPS on port 443 - this type of beaconing blends the malicious traffic with the legitimate traffic and can help the attacker evade firewalls.  
    DNS (Domain Name Server). The infected machine makes constant DNS requests to the DNS server that belongs to an attacker, this type of C2 communication is also known as DNS Tunneling.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/f7c6493a-3c12-4cca-8c8d-586d1e6c2f82)

## Actions on Objectives (Exfiltration)

This stage involves what the attacker can achieve or their original objectives e.g:

    Collect the credentials from users.
    Perform privilege escalation (gaining elevated access like domain administrator access from a workstation by exploiting the misconfiguration).
    Internal reconnaissance (for example, an attacker gets to interact with internal software to find its vulnerabilities).
    Lateral movement through the company's environment.
    Collect and exfiltrate sensitive data.
    Deleting the backups and shadow copies. Shadow Copy is a Microsoft technology that can create backup copies, snapshots of computer files, or volumes. 
    Overwrite or corrupt data.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/67d57131-581d-4b31-a6ac-51a31efaaf06)


## Practise Analysis

This task involved applying the cyber kill chain to a real-world scenario of an infamous cyber-attack in 2013.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/5b9a46e3-85f3-43f3-a294-80c3d269bd45)


![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/68c1c6ef-4ee1-4451-acdf-f702e67396bb)


## Conclusion

This room encapsulated the cyber kill chain, including each stage with its consultant task, whilst this can be seen as outdated due to its last modification date of 2011,it is still a great tool for improving
network defence.

