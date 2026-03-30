# Installation
This file covers setting up the vỉtual lab environment using UTM on macOS

## Requirements
	• MacOS M3
	• UTM installed
	• Ubuntu ISO file

## 1. Install UTM
• Download UTM from https://mac.getutm.app/

• Install the application

## 2. Download Ubuntu ISO
• Go to https://ubuntu.com/download

• Download Ubuntu Server ISO: ubuntu-24.04.4-live-server-arm64.iso

## 3. Create 03 Virtual Machine
• Open UTM, select "Create New VM"

• Select Virtualize: Linux

• Attach ISO file

• Configure CPU: 2 Cores, RAM: 2048Mb, Storage: 20Gb

## 4. Set Up Ubuntu
• Language: English

• Keyboard: Default

• Server Type: select Apple Ubuntu Server

• Network: Default

• Proxy: Empty

• Mirror: Default

• Storage: Use an entire disk

• Create user: Your name: , Server name: server1/2/3, User name: verra, Password: 

• SSH set up: select Install OpenSSH Server

• Feautured Server snaps: skip

• After installed -> reboot
