rbenv
===

This role allows you to install ruby using rbenv

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role: 

	# The user to install rbenv (i.e: www-data).
	user: www-data
	
	# Homedir, by default set to "/home"
	home: /export

	# Default version 1.9.3-p448
	ruby_version: 1.9.3-p125

	# Shell 
	sh: bash

Examples
--------

1) Install rbenv for the user who is connecting to the remote host.

	- hosts: all
	  roles:
	    	-  rbenv

2) Install rbenv for a given user, modifying the ruby version.

	- hosts: all
	  roles:
		- { role: rbenv, user: www-data, home: /var/www, ruby_version: 2.0.0-p195 }

3) Install rbenv for root user

	- hosts: all
	  roles:
		- { role: rbenv, user: root, home: /root, sh: zsh }


Dependencies
------------

None

License
-------

MIT

Author Information
------------------

Sergio Galván, more information on https://github.com/sgmac/rbenv
