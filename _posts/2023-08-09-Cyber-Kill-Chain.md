## Cyber Kill Chain

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/b250cc51-2ee7-4f01-9fcd-01203fcb18c1)

Type: #TryHackMe <br>
Links: https://tryhackme.com/room/cyberkillchainzmt <br>

This is a walkthrough for TryHackMe's Cyber Kill Chain room under the SOC Level 1 learning path.

Learning Objectives: In this room, you will learn about each phase of the Cyber Kill Chain Framework, and the advantages and disadvantages of the traditional Cyber Kill Chain. 

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
redirecting them to the malicious website of an attacker's choice. The attacker would look for a known vulnerability for the website and try to exploit it.
The attacker would encourage the victims to visit the website by sending "harmless" emails pointing out the malicious URL to make the attack work more efficiently. After visiting the website, 
the victim would unintentionally download malware or a malicious application to their computer. This type of attack is called a drive-by download. An example can be a malicious pop-up asking to download a fake
Browser extension.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/216c734a-274a-437d-ad5b-6fe013f255ed)

## Explotation







