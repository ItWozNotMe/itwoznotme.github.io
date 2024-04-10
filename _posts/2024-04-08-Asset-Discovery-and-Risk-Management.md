## Asset Discovery and Risk Management

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/1973298e-cf77-49e9-b59f-eb45743c41b9)

This is the current infrastructure of my homelab, showcasing the local netowork. As a design choice none of the services will be port fowarded, this lowers the attack surface as attacks can only happen inside of the network. However the threat modelling will showcase both external and internal vulnerabilities as more important for me to learn more contant than it is for me to be correct as the scenario is fabricated.

## Inventory of Assets

<h2 > Physical Assets </h2>

| Asset              | IP Address | Domain | Phyiscal Location |
|--------------------|------------|--------|-------------------|
| Raspberry Pi       |192.168.x.x | Local  | Home              |
| Personal PC        |192.168.x.x | Local  | Home              |
| Google Pixel 6     | Mobile 4G  |External| Home & External   |
| Google Pixel Watch |Shares Mobile Address | External | On Person |

<h2> Digital Assets </h2>

| Digital Asset | Port | Service | Severity | Description |
|---------------|------|---------|----------| ------------|
| SSH           | 22   | SSH     | Low      | Secure Method for Remote Access |
| Navidrome     | 4533 | HTTP    | Medium   | Muisc Application Via HTTP      |
| Homer         | 8080 | HTTP    | Medium   | Home Page Web Site              |
| UpTimeKuma    | 3001 | HTTPS   | Low      | Montioring Applcation           |

These two diagrams showcase all the devices in my local lan and additionally the services running and how server I have ranked them in terms of explotability. This is completed commercially to keep a log of all the assets, typically done along side a risk maanagement to calcualte quantitaive metrics. This can be revesited after a penetration test for a secondary evaluation.

<h2> nmap internal scan </h2>

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/c006f73e-f316-4fa9-b816-039050082761)

## Threat Modelling

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/2a840a70-c4f2-4c26-9c0e-0d839a8313cc)

Threat modelling is a process that involves a structured approach to identifying, assessing and mitigating threats; the diagram above showcasees the server, then each service, with potential vulnerbilities branching off, ranging from broad to some more specific. As this is a local server some of the attacks like DDoS and Brute force are not too much of a concern, whilst they can still happen the main focus is preventing devices that can access the internet (Compromised Clients) is the main concern.

## Risk Managment

