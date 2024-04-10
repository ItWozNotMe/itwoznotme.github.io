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

Annual Loss Expectancy is calcualted by assesing and dertermining an asset value (AV)
Identifying potential threats to each asset.

Firstly, the exposure factor (EF) needs to be determined for the threat for each asset, followed by calcualting the single loss expectancy (SLE) with the formulae ALE = SLE x ARO
The ARO is the annual rate of occurence, typically expressed as a decimal and is the likleihood of the incident occuring per year.

Determining the Single Loss Expectancy (SLE) is calculated using the formula SLE = AV x EF, this metric is used to determine the loss expectancy for a single occurrence event to a specific asset.

Example run through

| Digital Asset | AV   | EF      | ARO | SLE   | ALE   |
|---------------|------|---------|-----|-------|-------|
| SSH           | £100 | 0.50    |  4  |  £50  |  £200 |
| Navidrome     | £60  | 0.75    |  9  |  £45  |  £405 |   
| Homer         | £0   | 0.60    |  8  |  £0   |  £0   |          
| UpTimeKuma    | £10  | 0.25    |  4  |  £2.5 |  £10  |         

SLE SSH = £100 x 0.50 = £50
ALE SSH = £50 x 4 = £200

SLE Navidrome = £60 x 0.75 = £45
ALE Navidrome = £45 x 9 = £405

SLE Homer = £0 x 0.60 = £0
ALE Homer = £0 x 8 = £0

SLE UpTimeKuma = £10 x 0.25 = £2.5
ALE = £2.5 x 4 = £10


## Conclusion

This blog post invovled asset discovery and risk management, whilst being rather basic it was incredibly insightful to identify risks within my local network, whilst they are unlikely to be exploited due to the server's design choices it is important to see how risk is identified and calculated.

Important Takeaways:

    Single Loss Expectancy (SLE):
    SLE = AV x EF

    Annual Loss Expectancy (ALE):
    ALE = SLE x ARO
