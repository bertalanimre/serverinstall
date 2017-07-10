# serverinstall
Install NginX, PHP 5.6, MySQL 5.7, Varnish and Fail2Ban on CentOS 7+, RedHat 7+ servers

The only thing you might need to change is in line 44! Change the network interface name in the file "InitNewServer" if yours it not ETH0!

Adviced to run this script on VPS right after buying, first entering with root.

This scripts installs basically a webserver ready to use with the followings installed:
* NginX - Webserver
* PHP-FPM - for PHP websites
* MySQL 5.7 - Database
* Varnish - For faster website service
* Composer - For easier installation of Laravel 5+ websites
* Memcached - For better memory useage
* Fail2Ban - Intruder Prevention System

Install steps:
* git clone https://github.com/bertalanimre/serverinstall.git
* chmod +x InitNewServer
* sh InitNewServer

What the script does in order:
* Updates the system
* installs vim, mc wget and epel-release
* fetches and installs latest Mysql repository and mysql-community-server
* starts and enables mysqld
* installs remi repository
* installs nginx repository
* installs PHP-FPM 5.6 and latest NginX
* starts and enables php-fpm and nginx
* changes nginx configuration to use /etc/nginx/sites-enabled for config files
* restarts nginx
* installs git npm memcached httpd-tools and libpng-devel
* starts and enables memcached
* installs firewalld fail2ban and varnish
* sets up fail2ban to watch for ssh connections
* starts and enables fail2ban, varnish and firewalld
* copies the included varnish files into varnish configurations while saving the originals
* restarts varnish and nginx
* sets up firewall to allow http and https connections
* saves firewall configuration and lists all the zones and their settings
* installs composer from remi repo
* makes directories for proper nginx use
* lists out all the services and their status
* shows remaining tasks that needs to be done
