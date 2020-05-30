---
layout: post
comments: true
title: "Winget (Preview) - Windows Package Manager"
categories: blog
author:
- Bhavesh Vaghela
meta: "Springfield"
---

### What is Winget?
Winget is a native windows package manager tool from Microsoft. It is [open source](https://github.com/microsoft/winget-cli) and currently in preview as of 29th May, 2020.

Winget will support **Windows 10 Build 1707 and higher version**. If you are a windows insider (fast or slow ring) then you might already have winget installed. You can type winget -v in command prompt to confirm whether you have winget installed or not in your machine.

![Winget Version](/images/winget1.png)

### How to use Winget?
To install any package in winget, you have to type command - **winget install package-name**. For example to install power toys, type in **winget install powertoys**

![Winget Install](/images/winget2.png)


### What else Winget can do?
The following commands are available:
  - **install** - Installs the given application  
  -  **show** - Shows info about an application  
  -  **source** - Manage sources of applications
  -  **search** - Find and show basic info of apps
  -  **hash** - Helper to hash installer
  - **files** - validate  Validates a manifest file

![Winget Install](/images/winget3.png)

For example to see the information about powertoys which we installed, we can try command **winget show powertoys** and it will display information such as version, description, publisher, homepage etc about powertoys.

![Winget Install](/images/winget4.png)

### Conclusion
Winget will help us in automating the process of getting application in our machine. You can specify application and it will install it on your machine. No hassle to search online, download and install. 

Happy Coding.



