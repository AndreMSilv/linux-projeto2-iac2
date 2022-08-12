# linux-projeto2-iac2
Script para provisionamento de um servidor Apache .

#!/bin/bash

echo " Instalação..."

apt-get update 
apt-get upgrade -y
apt-get install apache2 -y
apt-get install unzip -y
cd / temp
wget https://github.com//denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
unzip main.zip
cd linux-site-dio-main
cp -R * /var/www/html/
