# SSH Configuration
This file enables secure remote access between servers

## Install SSH 
(If forget select OpenSSH when set up VM)

Command:

    sudo apt install -y openshh-server

## Check SSH status
Command:

    systemctl status ssh

In case if the status shows "inactive (dead)", I'll start SSH and recheck it
Command:

    sudo systemctl start ssh
    sudo systemctl status ssh

If the status shows "failed", I'll check for log errors

    jorurnalctl -u ssh

Some regular errors can be:

### 1. Config File Error

    /etc/ssh/sshd_config

Check for the errors

    sudo sshd -t

If detect any error, fix it by

    vim /etc/ssh/sshd_config

### 2. Duplicate Port (port 22 is occupied)
Check:

    ss -tulnp | grep 22

If there is a port error, I'll change the port in config file

### 3. Uninstall SSH
Install by command:

    sudo apt install openssh_server -y

After fix all the error, restart SSH by

    sudo systemctl status shh

Now "active (running)", I try to SSH from s1-s2, s1-s3

    ssh verra@192.168.1.147

First time SSH will be asked "Are you sure you want to continue connecting (yes/no/[fingerprint])?"

    Yes

Enter password

Then

    exit
    ssh verra@1922.168.1.125
    exit


## Generate SSH Key
The purpose is to not re-enter password when SSH between servers

On server 1, create SSH key

    ssh-keygen -t ed25519

SSH key default storage path: ~/.ssh/id_ed25519

After SHH key generated, there are 02 files as showed bellow

    .ssh/id_ed25519
    .ssh/id_ed25519.pub
  (Only .pub file can be copied to server)

## Copy Key to Server
Copy key to both server 2 and 3

    ssh-copy-id verra@192.168.1.147
    ssh-copy-id verra@192.168.1.125

## Test SSH Connection 
On server 1

    ssh verra@192.168.1.147
    exit
    ssh verra@192.168.1.125
    exit

## Verification
SSH login without entering password


