
```bash
sudo apt update
sudo apt install apache2 \
                 ghostscript \
                 libapache2-mod-php \
                 mysql-server \
                 php \
                 php-bcmath \
                 php-curl \
                 php-imagick \
                 php-intl \
                 php-json \
                 php-mbstring \
                 php-mysql \
                 php-xml \
                 php-zip
```

- apt

```bash
sudo mkdir -p /srv/www
sudo chown www-data: /srv/www
curl https://wordpress.org/latest.tar.gz | sudo -u www-data tar zx -C /srv/www
```

- file
- uri, get_url

`wordpress.conf`

```bash
<VirtualHost *:80>
    DocumentRoot /srv/www/wordpress
    <Directory /srv/www/wordpress>
        Options FollowSymLinks
        AllowOverride Limit Options FileInfo
        DirectoryIndex index.php
        Require all granted
    </Directory>
    <Directory /srv/www/wordpress/wp-content>
        Options FollowSymLinks
        Require all granted
    </Directory>
</VirtualHost>
```

- template, copy

```bash
sudo a2ensite wordpress
sudo a2dissite 000-default
```

- file(state: link,absent)

```bash
sudo a2enmod rewrite
```

- file
- apache2_module

```bash
sudo service apache2 reload
sudo systemctl reload apache2
```

- service(handler)

```bash
sudo apt install mysql-server mysql-client python3-mysql
```

- apt

```sql
CREATE DATABASE wordpress;
```

- mysql_db

```sql
CREATE USER wordpress@localhost IDENTIFIED BY '<your-password>';
GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,ALTER ON wordpress.* TO wordpress@localhost;
FLUSH PRIVILEGES;
```

- mysql_user

```bash
sudo service mysql start
```

- service(handler)

`wp-config.php`

```
blah blah...
```

- template

ACCESS TEST

