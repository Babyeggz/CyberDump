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

### Windows 10 VM Setup


### Windows 10 VM (Clone) Setup

### Kali 2019 VM Setup

### Ubuntu 18.04.2 VM Setup

## VPN Setup

## Frequently Asked Questions
[This](/Cyber%20Security%20Lab/LabFAQ.md) will take you to my LabFAQ.md where you can find some of my reasoning behind what I did in this guide.
