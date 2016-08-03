# serverinstall
Install NginX, PHP 5.6, MySQL 5.7, Varnish and Fail2Ban on CentOS 7+, RedHat 7+, Fedora 23+ servers

This scripts installs basically a webserver ready to use with the followings installed:
* NginX - Webserver
* PHP-FPM - for PHP websites
* MySQL 5.7 - Database
* Varnish - For faster website service
 *Composer - For easier installation of Laravel 5+ websites
* Memcached - For better memory useage
* Fail2Ban - Intruder Prevention System

The only thing you might need to change is in line 44! Change the network interface name if yours it not ETH0!
