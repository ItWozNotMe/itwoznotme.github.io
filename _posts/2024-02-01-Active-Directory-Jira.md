## Active Directory Helpdesk Setup

Aims:

    Demonstrate Active Directory Setup: Provide a step-by-step guide and insights into setting up a Windows 10 Active Directory environment covering server and client configurations.

    Illustrate Helpdesk Simulation: Showcase the process of using Jira to create and manage support tickets, mimicking a real-world helpdesk environment within the Windows Active Directory setup.

    Highlight Troubleshooting Scenarios: Present common issues that users might encounter in a Windows environment and demonstrate the troubleshooting process, emphasizing the role of Active Directory in issue resolution.

    Integrate Jira for Ticketing: Could you explain the benefits of using Jira as a ticketing system, how it streamlines helpdesk operations, and its integration with Active Directory for efficient user support?

Objectives:

    Provide a Detailed Active Directory Installation Guide: Walk readers through the installation and configuration of Windows Server for Active Directory, detailing the necessary steps to establish the domain.

    Create and Manage Support Tickets in Jira: Outline the process of creating, tracking, and resolving support tickets using Jira, focusing on integrating Jira with the Active Directory environment.

    Simulate Helpdesk Interactions: Describe a simulated helpdesk scenario, including creating a support ticket, troubleshooting the issue on the client side, and resolving it on the server side.

    Discuss Active Directory Features for User Management: Highlight key features of Active Directory related to user account management, group policies, and security, emphasizing their importance in a helpdesk setting.

    Explore Best Practices for Helpdesk in an AD Environment: Share best practices for managing a helpdesk within a Windows 10 Active Directory environment, covering user support, ticket prioritization, and communication strategies.

## Active Directory Setup

Active Directory was set in the past and was reinstalled using a snapshot a full set-up guide can be seen here: https://itwoznotme.github.io/2023/09/03/HomeLab-ActiveDirectory.html

To test if the configuration still works ping and nslookup were used to test connectivity.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/70d0a5fa-3822-4623-9932-f7b6122eec04)

After this, a new user was added called Ryan with a random password.

## Jira Helpdesk

To mimic a helpdesk environment Jira was used to raise a ticket from the client to the helpdesk team.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/064593d5-fceb-45bf-81ee-3bc0c5e92fb0)
![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/ed5e6a92-7d73-4ea5-aba7-cac14000fa65)

Accessing the Domain Controller, we can see that a ticket has arrived at the helpdesk team, and can then be assigned to a member and solved or escalated.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/8764fac2-a499-497f-8cf6-e876c53c04ee)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/58bd04c8-2c51-4d85-910a-9f0232af98a2)

The ticket was understood and solved by the helpdesk operator by resting the password within the users and computers section of active directory.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/adc9b185-5d95-4ed6-97f9-ca49dddf956a)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/a210365e-bc77-4c01-86bc-8e944ce33946)

The password was updated, allowing the user to log in via active directory. The ticket was then marked as resolved through Jira.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/16db4707-22ed-497e-aa2a-03bc09bd5e7e)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/8c27f36b-23c2-4ac6-82a8-e1be7a4c758f)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d58cacde-c64b-45e9-b789-763e9224bf86)

The client was then able to join the domain with their new credentials.

## Additional Jira Helpdesk

After the scenario was completed I tested more options within my helpdesk environment
