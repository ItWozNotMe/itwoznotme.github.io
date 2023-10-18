## Intro to Cyber Threat Intel

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/e543b86f-422b-4d45-a634-c89d7207464a)

This walkthrough will cover TryHackMe's Introduction to Cyber Threat Intel room.

Type: #TryHackMe <br>
Links:  https://tryhackme.com/room/cyberthreatintel 

## Cyber Threat Intelligence

Cyber Threat Intelligence (CTI) can be defined as evidence-based knowledge about adversaries, including their indicators, tactics, motivations, and actionable advice against them. 
These can be utilised to protect critical assets and inform cyber security teams and management business decisions.

The primary goal of CTI is to understand the relationship between your operational environment and your adversary and how to defend your environment against any attacks. You would seek this goal by developing your cyber threat context by trying to answer the following questions:

    Who’s attacking you?
    What are their motivations?
    What are their capabilities?
    What artefacts and indicators of compromise (IOCs) should you look out for?

With these questions, threat intelligence would be gathered from different sources under the following categories:

    Internal:
        Corporate security events such as vulnerability assessments and incident response reports.
        Cyber awareness training reports.
        System logs and events.
    Community:
        Open web forums.
        Dark web communities for cybercriminals.
    External
        Threat intel feeds (Commercial & Open-source)
        Online marketplaces.
        Public sources include government data, publications, social media, and financial and industrial assessments.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/1ef66adf-bcb3-47a1-913f-9b4c0e83273e)

## CTI Lifecycle

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/5a68e540-4166-469f-9d95-d8dd4a4ea263)

## Direction

Every threat intel program requires to have objectives and goals defined, involving identifying the following parameters:

    Information assets and business processes that require defending.
    Potential impact to be experienced on losing the assets or through process interruptions.
    Sources of data and intel to be used towards protection.
    Tools and resources that are required to defend the assets.

This phase also allows security analysts to pose questions related to investigating incidents.

## Collection

Once objectives have been defined, security analysts will gather the required data to address them. Analysts will do this by using commercial, private and open-source resources available. Due to the volume of data analysts usually face, it is recommended to automate this phase to provide time for triaging incidents.
## Processing

Raw logs, vulnerability information, malware and network traffic usually come in different formats and may be disconnected when used to investigate an incident. This phase ensures that the data is extracted, sorted, organised, correlated with appropriate tags and presented visually in a usable and understandable format to the analysts. SIEMs are valuable tools for achieving this and allow quick parsing of data.
## Analysis

Once the information aggregation is complete, security analysts must derive insights. Decisions to be made may involve:

    Investigating a potential threat through uncovering indicators and attack patterns.
    Defining an action plan to avert an attack and defend the infrastructure.
    Strengthening security controls or justifying investment for additional resources.


## Dissemination

Different organisational stakeholders will consume the intelligence in varying languages and formats. For example, C-suite members will require a concise report covering trends in adversary activities, financial implications and strategic recommendations. At the same time, analysts will more likely inform the technical team about the threat IOCs, adversary TTPs and tactical action plans.

## Feedback

The final phase covers the most crucial part, as analysts rely on the responses provided by stakeholders to improve the threat intelligence process and implementation of security controls. Feedback should be regular interaction between teams to keep the lifecycle working.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/da2a0b6e-c43f-4298-8c48-b90bdc1948fa)

## CTI Standards & 

Standards and frameworks provide structures to rationalise the distribution and use of threat intel across industries. They also allow for common terminology, which helps in collaboration and communication. Here, we briefly look at some essential standards and frameworks commonly used.
This section also highlights Mitre ATT&CK, TAXXI, STIX, Cyber Kill Chain & The Diamond Model which were previously covered within this learning path.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/b6b02eda-f210-4d9b-b127-46dc83c3ffad)

This room concludes with a practical analysis of an SIEM dashboard

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/0ec2c3ea-eca5-426c-92ed-5bd2bebe96c4)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/97ac1d7b-fafb-46c6-aa50-249729231c43)

