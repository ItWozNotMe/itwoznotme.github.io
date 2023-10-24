## Mal: Strings

Type: #TryHackMe
Links: https://tryhackme.com/room/malstrings

## What are Strings?

From a programming perspective, "strings" is the term given for data handled by an application. At a broader view, these pieces of data are used to store information such as text to numerical values.
However "strings" can be stored within the application itself - where no input is necessary from the user. For example, using the example of usernames and passwords is a great representation of the many types of information that may be stored as a "string".

We're all security-minded people here and know that writing down passwords isn't a very smart thing to do. However, developers are not quite so likeminded and often leave credentials in applications which are often essential i.e. An application that server needs to know the IP address of it. Arguably, an IP address is trivial in comparison to the sensitivity of a password - but both would be stored as strings.

## Practical

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/9810732b-fc10-4d22-aa2b-3e94dd3b45ba)

After downloading the task files, the exe file was converted to a txt using strings; a program that is commonly used in malware analysis to extact strings from the suspected binary.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/89c1853b-72d6-4db0-a285-d87bd184584d)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/c64960c3-9a1c-4df1-9b0c-b714435f2e91)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d41c91e4-77a1-4830-b70c-e15314522ff8)


## Strings in the context of malware

malware types such as botnets and ransomware rely upon information being stored within strings I.e. IP Addresses so that they are able to "call home" and connect to their "Command and Control" (C&C) server.

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/c6c96033-cffb-47e9-9470-0cef6597582c)

## Practical 2

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/d417c193-65c4-4cf5-b007-9149b2209b6c)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/cd43e13c-85af-4262-820e-56c91a0fe6e8)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/294e1996-dcd8-4c40-8c03-51f72f485c27)

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/4bd3dbad-f725-4d01-b451-97e6a75af8e6)

## Conclusion

![image](https://github.com/ItWozNotMe/itwoznotme.github.io/assets/74746341/f59e5ef6-dbfd-4e52-8835-4fe6409e3546)
