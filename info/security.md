---
layout: page
title: "Security"
---
{% include JB/setup %}


# [Start SSL](http://www.startssl.com/?app=0)

Have to make sure your "client" certificate is renewed every year, so that you can register new domains.  I think you can only do this within two weeks of expiration.  It's a bit painful to use, but it is free.


## Personal Validation Code

  * Login -> "Validations Wizard" -> "Email Validation", get the code and validate.
  * "Certificates Wizard" -> "S/MIME and Authentication Certificate" -> .... browser asks if you wanna install........ some more prompts and done.


## Generating a new certificate

  - Create a new private key 

```
openssl genrsa 2048 > www.example.com.key
or 
openssl genrsa -des3 2048 > www.example.com.key
```

  - Generate Request 

```
openssl req -new -sha256 -key www.example.com.key > www.example.com.csr
```

  - Fill in fields
  - Validate a Domain on startssl website
    - Validation Wizards -> Domain Name Validation
    - Enter top level domain (r15cookie.com in this instance)
    - Based on whois info on domain, should send email with validation code
    - Enter validation code in email.
  - Get CSR signed
    - Certificate Wizards -> Web Server SSL/TLS Certificate
    - Skip (already generated private key/CSR)
    - Copy/paste text of CSR into window
    - Will take a few seconds to process.  Click Continue
    - Select appropriate top-level domain. 
    - Add one sub-level domain (generally www)
    - Confirm information, then continue.
    - May have to wait a few hours to complete confirmation of new certificate

# External Links 

Useful article at [Open Source Replacement for Security Software](http://www.datamation.com/security/65-open-source-replacements-for-security-software-1.html)  Packages I found interesting (mostly untested by myself unless otherwise stated)

  * Security Scanners:
    * [GovReady Github](https://github.com/GovReady): An entire Government sponsored site that integrates open source tools into government standards.  Policies for CentOS and Ubuntu exist, as well as a lot of other resources.
    * [OpenSCAP](http://www.open-scap.org/page/Main_Page): Open source tool to read and evaluate system security based on SCAP standards
    * [Lynis](http://wiki.ipfire.org/en/addons/lynis/start):  Another security scanner for Linux/Unix systems, focusing around common standards and best practices.  Seems far easier to install and configure than OpenSCAP.  However, I have not tested either at this point.
  * [Endian](http://www.endian.com): Appliance for security and hotspot management
  * [IPFire](http://www.ipfire.org/): Linux based firewall distro
  * [MailScanner](http://www.mailscanner.info/):  Seems easier then attempting to roll Spamassassin, ClamAV, greylisting, etc.
  * [Odessa](http://odessa.sourceforge.net/): Alternative to Autopsy/Sleuth Kit for Open Source forensics work.
  * [PFSense](https://www.pfsense.org/):  Pretty solid when I last used the project a few years ago.  Based on FreeBSD, so limited to whatever FreeBSD supports hardware wise.
  * [Snort](https://www.snort.org/): Open source intrusion detection system.
