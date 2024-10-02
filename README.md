# docker_nginx
### 1.Create an account on aws
### 2.Sign in to your account 
### 3.Go to your dashboard
### 4.Click on launch instance
### 5.Enter your server name and select ubuntu 
### 6.Click on create new key pair
### 7.Enter your key pair name then select .ppk and click on create new key pair
### 8.In the network settings click on allow http traffic from the internet
### 9.Click on launch instance
### 10.Copy the public ipv4 address from your instance and download putty. 
### 11.Paste the ip address in host name   
### 12.Click on SSH then auth then credentials
### 13.Click browse and open the key pair you downloaded
### 14.Click accept then type ubuntu and then press enter 
### 15.Install docker using the command
```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
``` 
### 16.Now use the following docker commands
```bash
newgrp docker
```
```bash
docker ps
```
```bash
docker --version
```
### 17.Use the following commands to use ngnix
```bash
docker pull nginx
```
```bash
docker run --name docker-nginx -p 80:80 nginx
```
```bash
ctrl + c
```
```bash
docker ps -a
```
```bash
docker run --name docker-nginx -p 80:80 -d nginx
```
```bash
docker ps
```
```bash
docker stop docker-nginx
```
```bash
docker rm docker-nginx
```
```bash
mkdir -p ~/docker-nginx/html
```
```bash
cd ~/docker-nginx/html
```
```bash
vi index.html
```
```bash
docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/usr/share/nginx/html nginx
```
