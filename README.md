[![Build Status](https://travis-ci.org/ledongthuc/ansible.bower.svg?branch=master)](https://travis-ci.org/ledongthuc/ansible.bower)

Role Name
=========

  Install Bower and trigger to install packages.

Requirements
------------

  Ansible >= 1.2
  Better is linux

Role Variables
--------------

| Name            | Default          | Description  |
| --------------- |:---------------- |:------------ |
| bower_packages  | [] (empty list)  | List packages that you want to install. It supports bower.json and package's name |

  Each item in packages are defined in http://docs.ansible.com/ansible/bower_module.html

  Example installation stanalone package:
  
    bower_packages:
    - name: bootstrap 

  Example installation from package.json

    bower_packages:
    - path: /srv/my-website

Dependencies
------------

  ledongthuc.bower

Example Playbook
----------------

    - hosts: all 
      roles:
      - role: ledongthuc.bower
        bower_packages:
        - name: bootstrap
        - path: /srv/my-website

License
-------

  Apache 2.0

Author Information
------------------
  Thuc Le - ledongthuc[at]gmail.com
