
# Technologies

-   Apache 2
-   Laravel x.x
-   PHP 7.4
-   Composer 2.0.x

# Production

## Composer 2.0

Install composer 2.0

```
cd ~
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
sudo chmod +x /usr/local/bin/composer
composer --version

```

See:

> Composer version 2.1.6 2021-08-19 17:11:08

## Apache 2 and PHP 7.4

Install Apache 2 and PHP 7.4

```
sudo apt update
sudo apt install php7.4 php7.4-fpm php7.4-xml php7.4-ldap php7.4-mbstring php7.4-mysql php7.4-gd php7.4-curl apache2 libapache2-mod-fcgid curl
sudo systemctl status php7.4-fpm
sudo apt autoclean && sudo apt clean
sudo a2enmod actions fcgid alias proxy_fcgi
sudo service apache2 restart
```

## DataBase

### MySQL

#### Create

```
mysql -u root -p
CREATE DATABASE db_name CHARACTER SET utf8 COLLATE utf8_general_ci;
```

#### Privileges

```
GRANT ALL PRIVILEGES ON db_name.* TO db_user@'localhost' IDENTIFIED BY 'xxxZZZ';
FLUSH PRIVILEGES;
