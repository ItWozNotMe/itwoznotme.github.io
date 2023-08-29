![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d9a8f637-e3c8-4f3c-87e4-5f4fcb73e6fc)

Type: #TryHackMe <br>
Link: https://tryhackme.com/room/diamondmodelrmuwwg42 

This is a walkthrough for TryHackMe's Diamond Model under the SOC Level 1 learning path.

## Introduction


The Diamond Model is composed of four core features: adversary, infrastructure, capability and victim. Encapsulating 
essential concepts of intrusion analysis while providing a flexible framework to encompass new ideas and concepts. Its
purpose is to identify elements of an intrusion and is also used to aid non-technical parties in the outcome of an event.

## Adversery Definitions

Adversary Operator is the “hacker” or person(s) conducting the intrusion activity.

Adversary Customer is the entity that stands to benefit from the activity conducted in the intrusion. 
It may be the same person who stands behind the adversary operator, or it may be a separate person or group.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/6ddf707d-4374-4714-ab2c-4426432ccfa1)

## Victim Definitions

Victim – is a target of the adversary. A victim can be an organization, person, target email address, IP address, domain, etc. It's essential to understand the difference between the victim persona and the 
victim assets because they serve different analytic functions. 

Victim Personae are the people and organizations being targeted and whose assets are being attacked and exploited. 
These can be organization names, people’s names, industries, job roles, interests, etc.

Victim Assets are the attack surface and include the set of systems, networks, email addresses, hosts, IP addresses, 
social networking accounts, etc., to which the adversary will direct their capabilities.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/0c309c1e-69bb-4b6b-b127-73dd08b3097f)

## Capability Definitions

Capability – is also known as the skill, tools, and techniques used by the adversary in the event. 
The capability highlights the adversary’s tactics, techniques, and procedures (TTPs). 

Capability Capacity is all of the vulnerabilities and exposures that the individual capability can use. 

An Adversary Arsenal is a set of capabilities that belong to an adversary. 
The combined capacities of an adversary's capabilities make it the adversary's arsenal.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/a05383bb-ab20-4034-9a2f-dcf52c7b1d6c)

## Infrastructure Definitions


Infrastructure – is also known as software or hardware.
Infrastructure is the physical or logical interconnections that the adversary uses to deliver a capability or
maintain control of capabilities. For example, a command and control centre (C2) and the results from the victim 
(data exfiltration). 

Type 1 Infrastructure is the infrastructure controlled or owned by the adversary. 

Type 2 Infrastructure is the infrastructure controlled by an intermediary. 
Sometimes the intermediary might or might not be aware of it. 
This is the infrastructure that a victim will see as the adversary. 
Type 2 Infrastructure has the purpose of obfuscating the source and attribution of the activity. Type 2 Infrastructure includes malware staging servers, malicious domain names, compromised email accounts, etc.

Service Providers are organizations that provide services considered critical for the adversary availability of Type 1 and Type 2 Infrastructures, for example, Internet Service Providers, domain registrars, and webmail providers.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/016d00d4-133a-4378-bfe0-3a71c2542c73)

## Event Meta Features

Six possible optional features can be added resulting in valuable intelligence gained using the Diamond model:

  Timestamp
  Phase
  Result
  Direction
  Methodology
  Resources

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/82338dfe-5579-4f30-936f-4f3ea1c43df8)

## Social-Political Component/Technology Component

The social-political component describes the needs and intent of the adversary, for example, financial gain, gaining acceptance in the hacker community, hacktivism, or espionage. 

Technology – the technology meta-feature or component highlights the relationship between the core features: capability and infrastructure. The capability and infrastructure describe how the adversary operates and communicates. A scenario can be a watering-hole attack which is a methodology where the adversary compromises legitimate websites that they believe their targeted victims will visit.









