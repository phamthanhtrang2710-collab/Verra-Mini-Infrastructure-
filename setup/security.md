# Security Configuration
This file contains the basis security checks and firewall configuration steps

## Install UFW Firewall

    Sudo apt install -y ufw

## Enable UFW 

    sudo ufw enable
## Allow SSH

    sudo ufw allow SSH
## Allow Web

    sudo ufw allow 80/tcp
## Check status

    sudo ufw status
## Create file
On server 3

    Mkdir ~/labfiles
    cd  ~/labfiles
    vim notes.txt
    echo "MiniLab Practice" > notes.txt
    cat notes.txt
## Create New User

    adduser thi
## Create new group

    addgroup thi
## Align user to group

    usermod -aG thi thi
## Check existing group

    cat /etc/group
or

    grep testusers /etc/group

or

    getent group testusers
## Change Permissions

    chmod 600 notes.txt
## Change Owner

    chown thi:thi notes.txt
## Check permissions and owner

    ls -l
## Verification
Firewall rule applied

Users and groups created

Permissions and owner updated 
    
