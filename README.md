LAMP on Openstack
=================
This project will deploy under the help with Puppet Apache/PHP/MySQL on a Virtual Machine (VM) 
under the help of most of the standard Puppetlabs puppet modules. It's easy to adapt and to see, 
how it could work in an example: 
 

Features
--------

- install generated user account / ssh keys
- format and mount additional volumes
- set ntp client
- install MySQL Server with database and user
- install and configure Haproxy as SSL-Termination (needs >v1.5)
- provides ssl cert
- install apache with PHP and configured vhost
- install test web page
- provide monitoring with Nagios/Icinga (include pnp4nagios & SMS + Voice notification with Twilio service)
- builds a configuration package (deb/rpm) with fpm (using build.sh)


Requirements
------------
- Virtual Linux Machine (Ubuntu 14.04 trusty)
- 1 Floating IP
- 2 attached volumes

- Puppet client (at least version 3)


Usage
-----

Install server with all defaults (otherwise edit site.pp before apply puppet)

    dpkg -i lamp-conf_01-master-1435250897-1_amd64.db
	cd /etc/puppet
	puppet apply manifests/site.pp


Testing
-------

Developed for Ubuntu, will be expand. 


Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b my_markup`)
3. Commit your changes (`git commit -am "Added Snarkdown"`)
4. Push to the branch (`git push origin my_markup`)
5. Open a [Pull Request][1]
6. Enjoy a refreshing Diet Coke and wait


