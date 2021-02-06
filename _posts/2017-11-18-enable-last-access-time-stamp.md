---
layout: post
title: Enable last access timestamp
author: saman
image: assets/images/twemoji-spiral-calendar.svg
description: 
categories: [file system]
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
**Last access time** for files and folders is disabled by default in Windows 10 and 7. There are two ways to enable it.

## First method: Registry
Navigate to the following registery key:  
`Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\`  
and set the data of the `NtfsDisableLastAccessUpdate` value to `0`.

## Alternative method: Command Prompt
Alternatively, you can run the following line in the Command Prompt.
- To enable: &nbsp; `fsutil behavior set disablelastaccess 0`
- To disable:&nbsp; `fsutil behavior set disablelastaccess 1`

### References
- <https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/fsutil-behavior>
- <https://www.sevenforums.com/tutorials/243272-last-access-timestamp-enable-disable-windows.html>
