

# Start docker compose
docker-compose up -d

# Connect to mysql
This is the command
mysql -u root -p -h localhost


# Ubuntu php sources
deb https://ppa.launchpadcontent.net/ondrej/php/ubuntu jammy main 
deb-src https://ppa.launchpadcontent.net/ondrej/php/ubuntu jammy main 

# Sources ubuntu PHP
https://launchpad.net/~ondrej/+archive/ubuntu/php/


# Command to add sources
apt install ca-certificates
apt-get update
apt-get install gnupg
apt-get install gnupg2
apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4F4EA0AAE5267A6C

# How to Add keys
https://www.linuxuprising.com/2021/01/apt-key-is-deprecated-how-to-add.html


# Commit changes from container to image

docker commit f3e7eecdbbd5 ubuntu:apache-php

# Creater a container 
docker run --name mariadbh2s -p 3306:3306  -e MYSQL_ROOT_PASSWORD=password -d mariadb

# Ubuntu sources list file
/etc/apt/sources.list

# Get ubuntu version
lsb_release -a




# MariaDB/MySQL

MediaWiki will ask you for database and user name and will attempt to create them if they don't already exist. If doing so from MediaWiki is impossible, you can do this using various control panels such as PhpMyAdmin, which are often available from shared hosts, or you may be able to use ssh to login to your host and type the commands into a MySQL prompt. See the corresponding documentation. Alternatively, contact your host provider to have them create an account for you.

CREATE DATABASE wikidb;
CREATE USER 'wikiuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON wikidb.* TO 'wikiuser'@'localhost' WITH GRANT OPTION;

If your database is not running on the same server as your web server, you need to give the appropriate web server hostname — mediawiki.example.com in the example below — as follows:

GRANT ALL PRIVILEGES ON wikidb.* TO 'wikiuser'@'mediawiki.example.com' IDENTIFIED BY 'password';

# Enable PHP Modules

https://tecadmin.net/enable-disable-php-modules-ubuntu/

# Switch php versions on commandline ubuntu 16.04

https://stackoverflow.com/questions/42619312/switch-php-versions-on-commandline-ubuntu-16-04

# To enable PHP specific version
https://askubuntu.com/questions/912638/error-module-php7-0-does-not-exist