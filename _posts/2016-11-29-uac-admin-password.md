---
layout: post
title: Make Windows UAC require a password for the administrator
author: saman
image: 
description: 
categories: [security, uac]
tags: [windows 10, windows 7]
beforetoc: 
toc: false
rating: 
revision_date: 
featured: false
hidden: false

# Variables with default values in _config.yml
header: 
comments: 
footer-alertbar: 
footer-jumbotron: 
---
While the *User Account Control (UAC)* prompts in a standard account may require a password, this is not the case while using an admin account. Once logged into the Admin account, a user can change anything only by clicking Yes on a User Account Control box. By requiring a password on each UAC prompt you can add security to your administrator account.

In order for the UAC to require a password for administrators, in Windows 10 and 7:
1. In the Start menu, type in `Local Security Policy` and hit enter.
1. Once this program is open, navigate to: `Local Policies → Security Options`
1. Double click on `User Account Control: Behavior of the elevation prompt for administrators in Admin Approval Mode`
1. Select `Prompt for credentials` in the list, then click OK. (The default option is `Prompt for consent for non-Windows binaries`.)  
**Recommended Alternative:** You can choose `Prompt for consent`, to make the UAC prompt come up in all scenarios in which administrative permissions are needed, such as removing a file that needs administrative permission to delete.

## Note
In *Windows 10 Home Edition*, there is no access to *Local Group Policy Editor*, so to make the UAC prompt show up when trying to remove a file that is protected (needs administrative permission to delete), the only thing you can do is to change the UAC settings:
1. In the Start menu, type in `UAC` and select `Change User Account Control settings`.
1. Change the option to `Always Notify` and hit OK.
