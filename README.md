# Environment-setup-for-UBUNTU
Here you are advised to set up your ubuntu environment to run laravel projects with an Nginx server. You can seem to link your Nginx server with PHPMyAdmin. You can install MySQL server with PHP-8 on your ubuntu machine.

# Before Running Any Command You Need To Run
~~~
sudo apt update
~~~

# Then
~~~
sudo apt upgrade
~~~

# Install Curl
~~~
sudo apt install curl
~~~

# Install Nginx Server
~~~
sudo apt install nginx
~~~

# Install PHP 8
~~~
sudo apt install php8.0-fpm
~~~

# Install Nginx repository
~~~
sudo add-apt-repository ppa:ondrej/nginx
~~~

# To check the status of service
~~~
sudo systemctl status php8.0-fpm
~~~

# Nginx
~~~
sudo nginx -t
sudo systemctl restart nginx
~~~

# Install PHP 8 Extension
~~~
sudo apt-get install network-manager libnss3-tools jq xsel
sudo apt-get install php8.0-zip
sudo apt-get install php-mbstring
sudo apt-get install php8.0-curl
~~~

# Install Composer
~~~
curl -sS https://getcomposer.org/installer -o composer-setup.php
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
~~~

# Install valet
~~~
composer global require cpriego/valet-linux
test -d /.composer && bash /.composer/vendor/bin/valet install || bash ~/.config/composer/vendor/bin/valet install
~~~

# Install MySQL Server
~~~
sudo apt install mysql-server -y
sudo mysql
~~~

# Seem-link PHPmyadmin With MySQL Server
~~~
sudo apt install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
ln -s /usr/share/phpmyadmin /var/www/phpmyadmin
~~~

# Install Node JS
~~~
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt install nodejs
sudo apt-get install --reinstall nodejs-legacy     # fix /usr/bin/node
~~~

# Install Skype
~~~
sudo snap install skype
~~~

# For Cache Clear
~~~
journalctl --disk-usage
sudo journalctl --rotate
sudo journalctl --vacuum-time=2days
~~~

# For start the Snap
~~~
sudo systemctl start snapd
sudo systemctl enable snapd
~~~

# For Uninstall the Snap
~~~
sudo apt autoremove --purge snapd
~~~

# Install Snap
~~~
sudo apt install snapd
~~~

# Install VSCode
~~~
sudo snap install code --classic
~~~

# For Partition Disk
~~~
wget --version
wget https://dl.google.com/linux/direct/
google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
~~~