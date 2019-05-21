# Lab Setup Intro
This is guide to help you set up your own virtualized lab environment for penetration testing and malware analysis!

## Setup Overview
**My machine specs**- 2018 HDR Lenovo ThinkPad X1 Carbon (6th Gen) - Windows 10 Pro - Intel Quad Core i7-8650U, 1TB NVMe-PCIe SSD, 16GB RAM

    Host Machine (Windows 10)
        - Windows Defender Configurations (on)
        - UAC on “always notify”
        - Python 3 and JetBrains PyCharm
        - VMware Workstation Pro 
            - Windows 10 x64 VM
            - Windows 10 x64 VM (cloned)
                - Windows Defender Configurations (off)
                - Installed Malware Analysis Tools
            - Kali 2019 x64 VM
            - Ubuntu 18.04.2 x64VM
        - Norton VPN

## Host Machine Configurations
Assuming you are starting with a new computer or at least a fresh install of Windows 10 this how I am currently configuring my computer “out of the box.”

### Windows Defender Configuration
[Why use Windows Defender? FAQ](https://github.com/Babyeggz/CyberDump/blob/master/Cyber%20Security%20Lab/LabFAQ.md#q-why-windows-defender)

Navigate to Windows Defender Security Center.

`Windows Key -> type “Windows Security” and press enter`

I just make sure everything is turned on and I get all the green check marks.

<img src="https://i.gyazo.com/e79f7f1d7917141d24af05db00ad34e4.png" width="500">

Configure the rest of windows defender however you choose.

***WARNING*** Do not enable core isolation under under Device Security settings, this will prevent you from using virtual machines!

### User Account Control (UAC) Settings
Open User Account Control Settings

`Windows Key -> type “UAC” and press enter`

Feel free to adjust this setting as you wish but I recommend setting it to “always notify.” 

[Why put UAC on "always notify? FAQ](https://github.com/Babyeggz/CyberDump/blob/master/Cyber%20Security%20Lab/LabFAQ.md#q-why-set-user-account-control-uac-to-highest-setting)

## Python 3 and JetBrains PyCharm Installation and Setup
This is all pretty straight forward, for the purpose of saving time I will assume that you will not have any troubles with this part of the guide if you have installed things before. Here is a video computer science teacher that made a video for his students in his class covering this. It's only about 10 minutes long so dont worry. (I may come back and do a step by step myself for the guide)

Link to Mr. Gerry Jenkin's walkthough: https://www.youtube.com/watch?v=puBXxzcWJIQ

Link to Python 3 download: https://www.python.org/downloads/

Link to JetBrains PyCharm download: https://www.jetbrains.com/pycharm/download/#section=windows


## Virtualization Lab Installation and Setup
This part of the tutorial is very important and kind of the "meat and potatoes" of this whole thing. This (if done correctly) will hoefully give you a work environment that will keep you responsible and a lot safer when practiving penetration testing techniques and analyzing live malware. The lab provides an ethical and safe place for you to hack virtual machines without the need to ask permission or wonder if it is within the legal bounds while the Malware analysis virtual machine gives you an isolated work environment where you can safely perform static and dynamic analysis on live samples without the fear of spreading. ***Should I add a disclaimer for vm breakout?***

### VMware Workstation Pro
Once you have downloaded your VMware Workstation 15 Pro executable you need to run it and go through the installation wizard. It is retty straight forward and towards the end of the install you will need to enter your license key that you either obtained from a purchase from their website or your school software catalog. If you have any issues with the installation of the software you could follow [this person's guide on youtube](https://www.youtube.com/watch?v=OMIpKxZbfws).

***WARNING*** VMware Player will not work for the purposes of this lab as it does not offer snapshot functionality

[Why use Workstation Pro and not Virtualbox? FAQ](https://github.com/Babyeggz/CyberDump/blob/master/Cyber%20Security%20Lab/LabFAQ.md#q-why-are-you-using-vmware-workstation-pro-and-not-virtualbox)

### Windows 10 VM Setup

Go to https://www.microsoft.com/en-us/software-download/windows10 and click `Download tool now` to download the Windows 10 installation media tool. You will need this to make a Windows 10 ISO file to use for your virtual machine.

Run the Windows installation media tool that you just downloaded and select `Create installation media (USB flash drive, DVD, or ISO file) for another PC` and then click `Next`.

You may change your language on the next screen if you wish but I just leave these set to defaults and click `Next`.

Select `ISO file` and then click `Next` and choose a location on your computer for your ISO to be saved to. and click `Finish`.

Open VMware Workstation Pro if you havent already and from the home page click on `Create a New Virtual Machine`.

Select `Typical (recommended)` and click `Next`.

Select `Installer disc image file (iso):`, supply the path to where you saved the ISO you created earlier, and then click `Next`

Now you can name your VM whatever you would like, just make sure to give your VM a unique name because you may want to add more "Windows 10 VM" to your lab. When you are done click `Next`.

You can change your hard disk size on this page if you want, I leave mine at 60 GB which is my default. Select `Store virtual disk as a single file` and click `Next`.

Click on `Customize Hardware...`->`Add...`-> select `Network Adapter` and click `Finish`

Select `Network Adapter` -> select `Host-only: A private network shared only with the host`.

After that, you may configure your hardware settings however you may choose. Here is how mine is set up if you want to do the same.

<img src="https://i.gyazo.com/e88de309243f69a6f4e6cbfbf0baf28d.png" width="500">

If you are happy with your hardware settings then you can click `Close` and then click `Finish` to create the VM.


### Windows 10 VM (Clone) Setup

### Kali 2019 VM Setup

### Ubuntu 18.04.2 VM Setup

## VPN Setup
go to https://www.privateinternetaccess.com/pages/buy-vpn/ to purchase a PIA service subscription. I reccomend the 2 year plan because it greatly reduces the cost and really makes this provider shine over other providers.

After you enter payment information and a valid email that you can receive mail at, they will email you some temporary login credentials as well as redirect you to their download page to download the installer.

First go to your email and retrieve your username and password and click the link that they send you to go to their logon page of their website. Login using the username and temporary password that they give you. 

I **HIGHLY** encourage you to change your password here!

After you change your password go ahead and run the installer that you downloaded.

After you run the installer your are then met with this page:

<img src="https://i.gyazo.com/9323c4628fd1c83fedf5aaf1a45ad486.png" width="500">

You may wish to go through the tour or not, either way you end up at the login page. Go ahead and log into the PIA application with your provided username and the new password that you created.

Click on the 3 dots at the top of the 
## Frequently Asked Questions
[This](/Cyber%20Security%20Lab/LabFAQ.md) will take you to my LabFAQ.md where you can find some of my reasoning behind what I did in this guide.
