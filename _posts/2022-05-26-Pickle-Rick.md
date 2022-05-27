## Pickle Rick

![image](https://user-images.githubusercontent.com/74746341/170707048-b262ffdd-4143-4a88-b513-fa2e8970150c.png)


Type: #TryHackMe <br>
Links: https://tryhackme.com/room/walkinganapplication <br>
 
This room will allow me to start completing the 'Starter Series' on TryHackMe; a series of beginner ctfs to assist with developing my penetration testing skils.

Starting the Machine within TryHackMe, I opted to use a flag -sV with my nmap script to enumerate versions of the services running on the target machine, the command resulted the enumeration of port 22/ssh running OpenSSH 7.2p2 and port 80/http running Apache Version 2.4.18.

![image](https://user-images.githubusercontent.com/74746341/170707659-271cd971-b8bf-497c-84c4-4f66dc03fdaf.png)

Visting http://10.10.51.201/ yeilded a websever, there is no inital information on the webserver so I viewed the source of the page.

![image](https://user-images.githubusercontent.com/74746341/170709387-7a8ad1bc-3d87-47ba-bb7d-e456b7bea9cb.png)

Viewing the page source revealed the username 'R1ckRul3s', this is a common weakness
within web applications (CWE-312 : Cleartext Storage of Sensitive Information).

![image](https://user-images.githubusercontent.com/74746341/170709162-05d4ff82-9a46-4a03-8bab-efdaabc4821a.png)

Before using a tool like gobuster to brute force potential directories, I used common web files such as robots.txt to attempt to further enumerate the webserver.

![image](https://user-images.githubusercontent.com/74746341/170710128-d31bae39-27e0-49e2-806d-5faea0ed2302.png)

http://10.10.51.201/robots.txt contained 'Wubbalubbadubdub' which could be used alongside the username 'R1ckRul3s'.

I attempted to login to the SSH server on port 22 using these credentails, but was denied, meaning more enumeration on the webserver is needed.

![image](https://user-images.githubusercontent.com/74746341/170710724-cefd75c4-1a1d-4a72-b99e-278188a34739.png)

A gobuster scan quickly revealed /assets, visting http://10.10.51.201/assets/ reveals a number of files.

![image](https://user-images.githubusercontent.com/74746341/170710836-362088a1-680b-4214-8c14-b96bcbcca943.png)

This credentials can be used on a login page at http://10.10.51.201/login.php

![image](https://user-images.githubusercontent.com/74746341/170711587-c8477ba7-0a99-450f-8a68-cd93dc0a0341.png)

The credentials allow for succesful authentication and redirect to http://10.10.51.201/portal.php, on this page is an input box that allows for the exection of commands.

![image](https://user-images.githubusercontent.com/74746341/170711792-eb0187c0-297c-4263-be70-24d25dbd239a.png)

Using 'ls' to list directory contents results in a directory listing with 'Sup3rS3cretPickl3Ingred.txt', at this time the 'cat' command is not usable.

![image](https://user-images.githubusercontent.com/74746341/170712040-ca94173b-fac6-44a2-8e09-9516423513cf.png)

To attempt to gain a foothold I navigated to https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet and started a  listener on port 4444

![image](https://user-images.githubusercontent.com/74746341/170712591-c98ae0fa-379a-43cb-a9cb-c18a96190015.png)

To start I first used a perl reverse shell

![image](https://user-images.githubusercontent.com/74746341/170712728-9721a33e-4197-45c7-b276-8c07a36631a2.png)

Initial attempts at gaining a reverse shell did not work and instead I used a perl reverse shell from https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md

![image](https://user-images.githubusercontent.com/74746341/170714704-174f8471-71df-4b5a-aebb-f19f8f8451ff.png)

This resulted in a perl reverse shell, after this I can start retriving the flags for the ctf. The second ingredient being found within /home/rick, this also confirms the existance of a rick user. The final flag for the ctf likely requires additional privileges.

Using sudo -l displays that www-data can run any command without a password.

![image](https://user-images.githubusercontent.com/74746341/170717748-dbe72ff4-ba0f-4a5d-be63-3a7211eee59d.png)

Using "sudo su" results in root access, this can be confirmed using the "whoami" command.
The third flag can be found within /root.

This was a fairly easiy ctf, with the foothold into the machine being gained through CWE-312, allowing for access into /portal.php, where a vulnerable input box resulted in a reverse shell, and the lack of permissons resulted in an privilege escalation.


