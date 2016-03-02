Description
=========

[![Build Status](https://travis-ci.org/Yannik/ansible-role-secure-ssl-certs.svg?branch=master)](https://travis-ci.org/Yannik/ansible-role-secure-ssl-certs)

This role automatically secures keys and certificates in `/etc/ssl/`.

Requirements
------------

No requirements

Role Variables
--------------

It's recommended to use relative modes to only ever remove privileges
and not add privileges.

If you use an absolute mode like `640`, it would not be possible
to manually set a lower privilege of `600`.

* `secure_ssl_key_mode`: mode to set on ssl keys
    * Default: `g-wx,o-rwx`
* `secure_ssl_key_group`: group to set on ssl keys
    * Default: `root` 
* `secure_ssl_cert_mode`: mode to set on ssl certificates
    * Default: `g-wx,o-wx` 
* `secure_ssl_cert_group`: group to set on ssl certificates
    * Default: `root` 

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - role: Yannik.secure-ssl
           secure_ssl_key_group: 'ssl-cert'

License
-------

GPLv2

Author Information
------------------

Yannik Sembritzki
