---
layout: post
title: Flush the local DNS cache
author: saman
image: 
description: 
categories: [network, dns]
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
When opening a domain name in your web browser or elsewhere, sometimes you might notice that the domain name is not resolved into the correct IP address. This might happen because the DNS cache on your computer contains the incorrect IP mapping.

You can fix this issue by flushing (resetting) the local DNS cache:
1. Run *Command Prompt* as Administrator.
1. Enter the command: `ipconfig /flushdns`
