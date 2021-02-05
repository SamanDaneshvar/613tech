---
layout: post
title: Block an IP address in the hosts file
author: saman
image: https://1gew6o3qn6vx9kp3s42ge0y1-wpengine.netdna-ssl.com/wp-content/uploads/prod/sites/5/2020/12/cybersecurity-image.jpg
description: 
categories: [network]
tags: [windows all]
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
To block an IP address in Windows:
1. Open the file "C:\Windows\System32\drivers\etc\hosts" in a text editor.
1. In a new line at the end of the file type `127.0.0.1` followed by at least one space, followed by the domain name you want to block.
1. Save the hosts file. Done!

## How to find a hostname (IP address ⇄ domain name)
To find the hostname, you can use the following commands in the Command Prompt:

- `ping` displays the IP address of a domain name.  
- `nslookup` performs a reverse lookup on an IP address and displays its corresponding domain name.

## Example: Putting it all together
Assume we want to block the IP address `8.8.8.8`.

1. In Command Prompt we enter this command: `nslookup 8.8.8.8`
1. The output would be as follows:
```
Server:  UnKnown
Address: 10.10.120.1
​
Name:    google-public-dns-a.google.com
Address: 8.8.8.8
```
1. As we can see, the domain name corresponding to IP `8.8.8.8` is `google-public-dns-a.google.com`.
1. Next, we open the hosts file, and add the following line to it:  
`127.0.0.1    google-public-dns-a.google.com`
1. Save the hosts file, and done!
