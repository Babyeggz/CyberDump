# Lab Setup Intro
This is guide to help you set up your own virtualized lab environment for penetration testing and malware analysis!

## Setup Overview
**My machine specs**- 2018 HDR Lenovo ThinkPad X1 Carbon (6th Gen) - Windows 10 Pro - Intel Quad Core i7-8650U, 1TB NVMe-PCIe SSD, 16GB RAM

    Host Machine (Windows 10)
        1. Windows Defender Configurations (on)
        1. UAC on “always notify”
        1. JetBrains PyCharm
        1. VMware Workstation Pro 
            1. Windows 10 x64 VM
            1. Windows 10 x64 VM (cloned)
                1. Windows Defender Configurations (off)
                1. Installed Malware Analysis Tools
            1. Kali 2019 x64 VM
            1. Ubuntu 18.04.2 x64VM
        1. Norton VPN

## Host Machine Configurations
Assuming you are starting with a new computer or at least a fresh install of Windows 10 this how I am currently configuring my computer “out of the box.”

### Windows Defender Configuration
Navigate to Windows Defender Security Center.

`Windows Key -> type “Windows Security” and press enter`

I just make sure everything is turned on and I get all the green check marks.

![WindowsDefender](/Cyber%20Security%20Lab/screenshots/WindowsDefender.jpg)

Configure the rest of windows defender however you choose.

**WARNING** Do not enable core isolation under under Device Security settings, this will prevent you from using virtual machines!

### User Account Control (UAC) Settings
Open User Account Control Settings

`Windows Key -> type “UAC” and press enter`

Feel free to adjust this setting as you wish but I recommend setting it to “always notify.”

## JetBrains PyCharm Installation and Configuration

## Virtualization Lab Installation and Setup

### VMware Workstation Pro

### Windows 10 VM Setup

### Windows 10 VM (Clone) Setup

### Kali 2019 VM Setup

### Ubuntu 18.04.2 VM Setup

## VPN Setup

## Frequently Asked Questions
[This](/Cyber%20Security%20Lab/LabFAQ.md) will take you to my LabFAQ.md where you can find some of my reasoning behind what I did in this guide.
