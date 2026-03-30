# Docker Set Up
This file contains the Docker installation and runs containers

## Install Docker
On server 1

    sudo apt install -y docker.io

Start Docker

    sudo systemctl enable docker
    sudo systemctl start docker

Check Docker status

    sudo systemctl status docker

Check Docker version

    docker --version

Run Docker without sudo

    usermod -aG docker $USER

then logout and login, or reboot

Check Docker

    groups

## Run Nginx Container
On server 1

    docker run -d --name mynginx -p 8080:80 nginx

## List Running Containers

    docker ps
## Check Nginx Containers
On server 1

    curl http://192.168.1.123:8080

On server 2

    curl http://192.168.1.123:8080

Nginx's htlm will appear
## Verification
Nginx container is running

Accessible via browser


    
