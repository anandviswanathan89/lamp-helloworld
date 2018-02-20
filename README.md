# lamp-helloworldlamp
my first lamp application

## brew tap - required
    brew tap homebrew/homebrew-php

## install php and mysql
    brew update
    brew install php56
    brew install php56-mcrypt
    brew install mysql

## mysql server
    mysql.server start
    mysql.server stop

## webserver
    sudo apachectl start
    sudo apachectl stop

Uncomment php module and restart webserver
    sudo vi /etc/apache2/httpd.conf

## default index path
    /Library/WebServer/Documents/


    cd /usr/local/mysql/bin ( navigate to mysql bin folder)
    ./mysql -u root -p ( then password given in installation) ( starting MySQL)

alter user "root"@"localhost" identified by "NEW PASSWORD"; ( changes mysql password to password in last field )
Download phpMyAdmin
Extract in /Library/WebServer/Documents and rename phpmyadmin

    cd /Library/WebServer/Documents ( navigate to webserver)
    sudo chmod o+x phpmyadmin/ ( give folders some rights )
    cd phpmyadmin ( navigate into phpmyadmin)
    mkdir config ( create config folder )
    sudo chmod o+x config ( give folder some rights )

Open browser and go to localhost/phpmyadmin/setup
Click on "New Server" and in the authentication tab, enter the password in the password field under "root"
    sudo mkdir /var/mysql ( create mysql folder in /var)
    sudo ln -s /tmp/ var/mysql/mysql.sock ( create symlink ) 
