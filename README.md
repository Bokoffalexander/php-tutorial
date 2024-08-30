[1 # How To Install PHP 8.3](#-1-how-to-install-php-8.3)

[2 # How To Install Composer](#2-#-How-To-Install-Composer)

[3 # MySQL Installation guide](#3-#-MySQL-Installation-guide)

[4 # How To Install NGINX Server](#4-#-How-To-Install-NGINX-Server)

[5 # How To Install Apache Server](#5-#-How-To-Install-Apache-Server)

[6 # How To Install Laravel](#6-#-How-To-Install-Laravel)

###############################

#-1-# How To Install PHP 8.3

###############################

sudo add-apt-repository ppa:ondrej/php

sudo apt update

sudo apt install php8.3-fpm php8.3-sqlite3 php8.3-mysql php8.3-common php8.3-cli

sudo systemctl restart apache2

###############################

###############################


###############################

# 2 # How To Install Composer

###############################

sudo apt update

###############################

## Загрузите установщик Composer с его официальной страницы:

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

###############################

## Следующая команда выполняет его локальную инсталляцию:

php composer-setup.php

###############################

## Для запуска глобальной установки выполните следующую команду:

php composer-setup.php --install-dir=/usr/local/bin --filename=composer

###############################

###############################

###############################

# 3 # MySQL Installation guide

###############################

sudo apt update

sudo apt install mysql-server

sudo systemctl restart mysql

###############################

## Вход

sudo mysql

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';

mysql -u root -p

CREATE DATABASE laravel;

exit

###############################

###############################


###############################

# 4 # How To Install NGINX Server

###############################

sudo apt update

sudo apt install nginx

sudo systemctl restart nginx

###############################

###############################

###############################

# 5 # How To Install Apache Server

###############################

sudo apt update

sudo apt install apache2 -y

sudo systemctl restart apache2 -y

###############################

###############################

###############################

# 6 # How To Install Laravel

###############################

composer create-project laravel/laravel example-app

cd example-app

php artisan migrate

php artisan serve

###############################

###############################
