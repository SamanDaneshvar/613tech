---
layout: post
title: Create a shortcut for any 'modern' Windows 10 app
author: saman
image: assets/images/rocket.svg
description: 
categories: [apps]
tags: [windows 10]
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
Windows 10 has a number of 'modern' apps, including Calculator, Camera, and Voice Recorder. These apps have different behavior from regular apps. For instance, you cannot easily launch them using a command in Command Prompt or using automation tools such as AutoHotkey.

To overcome this, we will create a shortcut to the app and then run that shortcut using a command in Command Prompt, etc.

## Steps
1. Launch *Run* and open the following:  
`shell:::{4234d49b-0245-4df3-b780-3893943456e1}`  
You can also copy this into the address bar of a Windows Explorer window.
1. This should open a secret folder named *Applications*.
1. Find the app you are looking for, right-click on it, and select *Create shortcut*.
1. Store the shortcut to your desired location.
1. You can now run this shortcut using AutoHotkey, etc. to launch the 'modern' Windows 10 app.

### Reference
<https://www.lifehacker.com.au/2015/08/how-to-create-a-shortcut-for-any-modern-windows-app/>
