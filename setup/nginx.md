# Nginx Web Server
This file sets up the basis web server using Nginx
## Install Nginx
On server 2

    sudo apt install -y nginx

## Enable and Start service

    sudo systemctl enable nginx
    sudo systemctl start nginx

## Check status

    sudo systemctl status nginx
    
## Test access
On server 2

    curl http://10.190.139.5

On server 1

    curl http://10.190.139.5

## Edit Web Page
On server 2

    vim /var/www/html/index.html

    <!DOCTYPE html>
    <html>
      <head>
        <title>Welcome to Verra Mini Infrastructure Project</title>
      </head>
      <body>
        <h1>Hello, thank you for watching this</h1>
        <p>This web server is running on Ubuntu and Nginx</p>
      </body>
    </html>
## Restart Nginx

    sudo systemctl restart nginx

## Verification

Custom web page is displayed

Access server IP in brower
