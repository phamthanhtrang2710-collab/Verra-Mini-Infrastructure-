# Networking
This file configures basic networking between VMs

## Configure IP Address
Command:

    ip a
Or

    hostname -I

(Write down the IP address)

• Server 1: 10.190.139.4

• Server 2: 10.190.139.5

• Server 3: 10.190.139.6

## Test Connectivity
From server 1 to server 2

Command:

    ping -c 4 10.190.139.5

Reverse:

    ping -c 4 10.190.139.4

From server 1 to server 3, and reverse

    ping -c 4 10.190.139.6 (on S1)
    ping -c 4 10.190.139.4 (on S3)

## Set Hostname (If Needed)
Command:

    sudo hostnamectl set-hostname server1

## Verification
• Server can ping each other

• Hostname update correctly
