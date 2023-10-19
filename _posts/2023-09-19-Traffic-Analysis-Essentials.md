## Traffic Analysis Essentials

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/e778cca1-4399-4265-b470-41cb390e4e38)

Type: #TryHackMe
Links: https://tryhackme.com/room/trafficanalysisessentials



Network Security is a set of operations for protecting data, applications, devices and systems connected to the network. 
It is accepted as one of the significant subdomains of cyber security. 
It focuses on the system design, operation and management of the architecture/infrastructure to provide network accessibility, integrity, continuity and reliability. Traffic analysis (often called Network Traffic Analysis) is a subdomain of the Network Security domain, and its primary focus is investigating the network data to identify problems and anomalies. 

Network Security

The essential concern of Network Security focuses on two core concepts: authentication and authorisation. There are a variety of tools, technologies, and approaches to ensure and measure implementations of these two key concepts and go beyond to provide continuity and reliability. Network security operations contain three base control levels to ensure the maximum available security management.

Base Network Security Control Levels:
Physical	Physical security controls prevent unauthorised physical access to networking devices, cable boards, locks, and all linked components.
Technical	Data security controls prevent unauthorised access to network data, like installing tunnels and implementing security layers.
Administrative	Administrative security controls provide consistency in security operations like creating policies, access levels and authentication processes.

There are two main approaches and multiple elements under these control levels. The most common elements used in network security operations are explained below.

The main approaches:
Access Control	Threat Control
The starting point of Network Security. It is a set of controls to ensure authentication and authorisation. 	
Detecting and preventing anomalous/malicious activities on the network. It contains both internal (trusted) and external traffic data probes.

The key elements of Access Control:
Firewall Protection
	Controls incoming and outgoing network traffic with predetermined security rules. Designed to block suspicious/malicious traffic and application-layer threats while allowing legitimate and expected traffic.
Network Access Control (NAC)
	Controls the devices' suitability before access to the network. Designed to verify device specifications and conditions are compliant with the predetermined profile before connecting to the network.
Identity and Access Management (IAM)	Controls and manages the asset identities and user access to data systems and resources over the network.
Load Balancing	Controls the resource usage to distribute (based on metrics) tasks over a set of resources and improve overall data processing flow.
Network Segmentation
	Creates and controls network ranges and segmentation to isolate the users' access levels, group assets with common functionalities, and improve the protection of sensitive/internal devices/data in a safer network.
Virtual Private Networks (VPN)
	Creates and controls encrypted communication between devices (typically for secure remote access) over the network (including communications over the internet).
Zero Trust Model	Suggests configuring and implementing the access and permissions at a minimum level (providing access required to fulfil the assigned role). The mindset is focused on: "Never trust, always verify".

The key elements of Threat Control:
Intrusion Detection and Prevention (IDS/IPS)
	Inspects the traffic and creates alerts (IDS) or resets the connection (IPS) when detecting an anomaly/threat.
Data Loss Prevention (DLP)
	Inspects the traffic (performs content inspection and contextual analysis of the data on the wire) and blocks the extraction of sensitive data.
Endpoint Protection
	Protecting all kinds of endpoints and appliances that connect to the network by using a multi-layered approach like encryption, antivirus, antimalware, DLP, and IDS/IPS.
Cloud Security	Protecting cloud/online-based systems resources from threats and data leakage by applying suitable countermeasures like VPN and data encryption.
Security Information and Event Management (SIEM)
	Technology that helps threat detection, compliance, and security incident management, through available data (logs and traffic statistics) by using event and context analysis to identify anomalies, threats, and vulnerabilities.
Security Orchestration Automation and Response (SOAR)
	Technology that helps coordinate and automates tasks between various people, tools, and data within a single platform to identify anomalies, threats, and vulnerabilities. It also supports vulnerability management, incident response, and security operations.
Network Traffic Analysis & Network Detection and Response	Inspecting network traffic or traffic capture to identify anomalies and threats.

Typical Network Security Management Operation is explained in the given table:
Deployment	Configuration	Management	Monitoring	Maintenance

    Device and software installation
    Initial configuration
    Automation

	

    Feature configuration
    Initial network access configuration

	

    Security policy implementation
    NAT and VPN implementation
    Threat mitigation

	

    System monitoring
    User activity monitoring
    Threat monitoring
    Log and traffic sample capturing

	

    Upgrades
    Security updates
    Rule adjustments
    Licence management
    Configuration updates

Managed Security Services

Not every organisation has enough resources to create dedicated groups for specific security domains. There are plenty of reasons for this: budget, employee skillset, and organisation size could determine how security operations are handled. At this point, Managed Security Services (MSS) come up to fulfil the required effort to ensure/enhance security needs. MSS are services that have been outsourced to service providers. These service providers are called Managed Security Service Providers (MSSPs). Today, most MSS are time and cost effective, can be conducted in-house or outsourced, are easy to engage, and ease the management process. There are various elements of MSS, and the most common ones are explained below.
Network Penetration Testing 	Assessing network security by simulating external/internal attacker techniques to breach the network.
Vulnerability Assessment	Assessing network security by discovering and analysing vulnerabilities in the environment.
Incident Response
	An organised approach to addressing and managing a security breach. It contains a set of actions to identify, contain, and eliminate incidents.
Behavioural Analysis	An organised approach to addressing system and user behaviours, creating baselines and traffic profiles for specific patterns to detect anomalies, threats, vulnerabilities, and attacks.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/5209c62a-d1e4-4983-b8d7-b9db9e45a74c)

## Traffic Analysis

Traffic Analysis is a method of intercepting, recording/monitoring, and analysing network data and communication patterns to detect and respond to system health issues, network anomalies, and threats. The network is a rich data source, so traffic analysis is useful for security and operational matters. The operational issues cover system availability checks and measuring performance, and the security issues cover anomaly and suspicious activity detection on the network. 

Traffic analysis is one of the essential approaches used in network security, and it is part of multiple disciplines of network security operations listed below:

    Network Sniffing and Packet Analysis
    Network Monitoring 
    Intrusion Detection and Prevention
    Network Forensics
    Threat Hunting 

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/76078d5a-561d-4fc9-8bee-a1636dcec13f)


