## Threat Intelligence Tools

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/4dd86fac-dd3e-4b0d-90b1-e935921a7c53)

Type: # TryHackMe
Links: https://tryhackme.com/room/threatinteltools

This room will cover the concepts of Threat Intelligence and various open-source tools that are useful. The learning objectives include:

    Understanding the basics of threat intelligence & its classifications.
    Using UrlScan.io to scan for malicious URLs.
    Using Abuse.ch to track malware and botnet indicators.
    Investigate phishing emails using PhishTool
    Using Cisco's Talos Intelligence platform for intel gathering.

## Threat Intelligence

Threat Intelligence is the analysis of data and information using tools and techniques to generate meaningful patterns on how to mitigate against potential risks associated with existing or emerging threats targeting organisations, industries, sectors or governments.

Mitigating Risks can be achieved by attempting to answer some questions: 

    Who's attacking you?
    What's their motivation?
    What are their capabilities?
    What artefacts and indicators of compromise should you look out for?

TryHackMe has defined some classifications of threat intel, listed below: 

    Strategic Intel: High-level intel that looks into the organisation's threat landscape and maps out the risk areas based on trends, patterns and emerging threats that may impact business decisions.
    Technical Intel: Looks into evidence and artefacts of attack used by an adversary. Incident Response teams can use this intel to create a baseline attack surface to analyse and develop defence mechanisms.
    Tactical Intel: Assesses adversaries' tactics, techniques, and procedures (TTPs). This intel can strengthen security controls and address vulnerabilities through real-time investigations.
    Operational Intel: Looks into an adversary's specific motives and intent to perform an attack. Security teams may use this intel to understand the critical assets available in the organisation (people, processes, and technologies) that may be targeted.

## Urlscan.io

Urlscan.io is a free service developed to assist in scanning and analysing websites. It is used to automate the process of browsing and crawling through websites to record activities and interactions.

When a URL is submitted, the information recorded includes the domains and IP addresses contacted, resources requested from the domains, a snapshot of the web page, technologies utilised and other metadata about the website.

## Scan Results

URL scan results provide ample information, with the following key areas being essential to look at:

    Summary: Provides general information about the URL, ranging from the identified IP address, domain registration details, page history and a screenshot of the site.
    HTTP: Provides information on the HTTP connections made by the scanner to the site, with details about the data fetched and the file types received.
    Redirects: Shows information on any identified HTTP and client-side redirects on the site.
    Links: Shows all the identified links outgoing from the site's homepage.
    Behaviour: Provides details of the variables and cookies found on the site. These may be useful in identifying the frameworks used in developing the site.
    Indicators: Lists all IPs, domains and hashes associated with the site. These indicators do not imply malicious activity related to the site.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/8e2a7e24-388b-44f1-a901-4488d2fb255b)

## Abuse.ch

Abuse.ch is a research project hosted by the Institute for Cybersecurity and Engineering at the Bern University of Applied Sciences in Switzerland. It was developed to identify and track malware and botnets through several operational platforms developed under the project. These platforms are:

    Malware Bazaar:  A resource for sharing malware samples.
    Feodo Tracker:  A resource used to track botnet command and control (C2) infrastructure linked with Emotet, Dridex and TrickBot.
    SSL Blacklist:  A resource for collecting and providing a blocklist for malicious SSL certificates and JA3/JA3s fingerprints.
    URL Haus:  A resource for sharing malware distribution sites.
    Threat Fox:  A resource for sharing indicators of compromise (IOCs).

This section involves using each site to answer questions on the given intel.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/14e4f75b-e284-4f51-968b-fc2a24d8e011)

## PhishTool

This task will introduce you to a tool, PhishTool, that you would add to your toolkit of email analysis tools. 

## Email Phishing

Email phishing is one of the main precursors of any cyber attack. Unsuspecting users get duped into opening and accessing malicious files and links sent to them by email, as they appear to be legitimate. As a result, adversaries infect their victims’ systems with malware, harvesting their credentials and personal data and performing other actions such as financial fraud or conducting ransomware attacks.

PhishTool seeks to elevate the perception of phishing as a severe form of attack and provide a responsive means of email security. Through email analysis, security analysts can uncover email IOCs, prevent breaches and provide forensic reports that could be used in phishing containment and training engagements.

PhishTool has two accessible versions: Community and Enterprise. We shall mainly focus on the Community version and the core features of this task. Sign up for an account via this link to use the tool.

The core features include:

    Perform email analysis: PhishTool retrieves metadata from phishing emails and provides analysts with the relevant explanations and capabilities to follow the email’s actions, attachments, and URLs to triage the situation.
    Heuristic intelligence: OSINT is baked into the tool to provide analysts with the intelligence needed to stay ahead of persistent attacks and understand what TTPs were used to evade security controls and allow the adversary to social engineer a target.
    Classification and reporting: Phishing email classifications are conducted to allow analysts to take action quickly. Additionally, reports can be generated to provide a forensic record that can be shared.

Additional features are available on the Enterprise version:

    Manage user-reported phishing events.
    Report phishing email findings back to users and keep them engaged in the process.
    Email stack integration with Microsoft 365 and Google Workspace.

This section involves using Thunderbird to answer a series of questions

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/cc0227f1-b4dc-4095-87b4-1972a2cbd31b)

Using ThunderBird I can see that the adversary is posing as Linkedin to trick the user, alongside the sender and receiver email address.
After this opening, the text file of Email1.eml reveals the sender's IP and can be defanged using CyberChef.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/1b7903c8-8a09-4343-88ed-ba0513c912de)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/2ea8c53c-8cbb-4e26-9b15-f6455780249e)

The last question can be answered by counting how many times the email was received.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/12073e57-8776-4f7b-a6b6-ba30ed18ff20)

## Cisco Talos Intelligence

IT and Cybersecurity companies collect massive amounts of information that could be used for threat analysis and intelligence. Being one of those companies, Cisco assembled a large team of security practitioners called Cisco Talos to provide actionable intelligence, visibility on indicators, and protection against emerging threats through data collected from their products. The solution is accessible as Talos Intelligence.

Cisco Talos encompasses six key teams:

    Threat Intelligence & Interdiction: Quick correlation and tracking of threats provide a means to turn simple IOCs into context-rich intel.
    Detection Research: Vulnerability and malware analysis is performed to create rules and content for threat detection.
    Engineering & Development: Provides the maintenance support for the inspection engines and keeps them up-to-date to identify and triage emerging threats.
    Vulnerability Research & Discovery: Working with service and software vendors to develop repeatable means of identifying and reporting security vulnerabilities.
    Communities: Maintains the image of the team and the open-source solutions.
    Global Outreach: Disseminates intelligence to customers and the security community through publications.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/37f06067-2a97-45f3-b162-13de4cc7b749)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/934c0c7d-6dc8-4c65-8322-8d5f436cb4a2)

The last section of the room involves using Phishtool alongside VirusTotal and Talos Intelligence to leverge intel on the phising emails.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/cf07539f-bfbd-4c3d-8f33-06a0611848ac)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/4f7c38af-ad67-497d-9f09-2245e54a0c6a)

Next Steps:
    https://tryhackme.com/room/yara
    https://tryhackme.com/room/misp
    https://tryhackme.com/room/redteamthreatintel

