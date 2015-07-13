---
layout: post
category : 
tags : [vagrant]
---
{% include JB/setup %}

Vagrant is one of the most useful tools for automating the build of Virtual environments for testing and development purposes.  I'm usually a Linux/Unix type guy, but on occation it would be nice to be able to test Windows.  
I just came across [this post](http://blog.syntaxc4.net/post/2014/09/03/windows-boxes-for-vagrant-courtesy-of-modern-ie.aspx) that indicates the modern.ie has provided 
a set of [base boxes](https://www.modern.ie/en-us/virtualization-tools#downloads) that are usable for Vagrant.  I haven't had a chance to test them yet, but plan to do so soon.

On another point, I didn't even know about [ModernIE](https://www.modern.ie/en-us)!  Not that I'm a huge IE fan, but seems like a really useful resource for web developers to test their site on older IE/OS combinations.  

**Edit:**  It appears that the VMs are only a Virtualbox image, not necessarily in a Vagrant-friendly configuration (WinRM enabled, etc, etc)  I might go on a search for more appropriate Vagrant images.  Still a useful resources, just not as integrated into Vagrant as one would hope.




