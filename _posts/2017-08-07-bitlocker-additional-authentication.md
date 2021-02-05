---
layout: post
title: Bitlocker - Require additional authentication at startup
author: saman
image: assets/images/emoji-locked-with-key-twitter.svg
description: 
categories: [encryption, security]
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
BitLocker uses *TPM (Trusted Platform Module)*, and by storing the encryption key in the TPM, decrypts the encrypted system drive automatically, without a need for passwords.

You can set BitLocker to ask for a PIN or a password at startup, in addition to using the key stored in TPM.

## Step 1: Allow additional authentication at startup
First, you need to allow multi-factor authentication at startup:

1. Go to Control Panel, and search for group policy, then click on Edit group policy.  
Alternatively, open Run and enter `gpedit.msc`.
1. In the Local Group Policy Editor window, navigate to:  
`Computer Configuration → Administrative Templates → Windows Components → BitLocker Drive Encryption → Operating System Drives`
1. Open the setting named Require additional authentication at startup, select the Enabled radio button, and click OK.  
Optional: To make sure Bitlocker won't encrypt your drive without taking advantage of TPM:  
`[Uncheck] Allow BitLocker without a compatible TPM`

## Step 2: Set a PIN for BitLocker
You can now change the settings for BitLocker:

1. Go to Control Panel → BitLocker Drive Encryption
1. Click on Change how drive is unlocked at startup
1. Choose the option you want:
- Enter a PIN: Requires a PIN at startup
- Insert a USB flash drive: Requires a flash drive containing the encryption key
- Let BitLocker automatically unlock my drive: Requires no additional authentication at startup

### Side note: TPM management
For TPM Management, open Run and enter `tpm.msc`.

### References
- For more information, read the BitLocker security considerations section at: <https://technet.microsoft.com/en-us/library/cc732774(v=ws.11).aspx>
- More information on BitLocker countermeasures and protection: <https://technet.microsoft.com/en-us/library/dn632176(v=ws.11).aspx>
- BitLocker FAQ: <https://technet.microsoft.com/en-us/library/cc766200(v=ws.10).aspx>
