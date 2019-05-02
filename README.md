Ansible Role Eliel
=========

This role was built to automate the process installing HTTPD package on servers.

Requirements
------------

Ansible > 2.0.0.2
Python > 2.7

Remote Server Requirements:
--------------
CentOS 7 or new


Role Variables
--------------

In order to make the settings easy, some Apache settings are located on file defaults/main.yml.
The following settings can be set:
httpd_listen_ip - the IP that will answer on the defined port
httpd_listen - the port that will answer to HTTP requests

If httpd_listen_ip is set as '*', the playbook will ignore and maintain the default port (80)

If you changed the port, remember to access the server as follows:
http://<your IP>:<port set>

If you don't know your IP, just type ifconfig in your terminal.


Example Playbook
----------------

In order to run, first you need to make sure that the httpd rpm file is located on the files folder. If you don't have the package, you can download from http://mirror.centos.org/centos/7/os/x86_64/Packages/ or directly from Apache Website (https://archive.apache.org/dist/httpd/).

Assuming that the file is proper located on the folder, you can use the following playbook as an example:
---
- hosts: all
  roles:
   - {role: textkernel_eliel}

Remember, in the first line, where is written hosts: all you can change to the name of your servers group.

License
-------

BSD

Author Information
------------------

Eliel Teotonio de Oliveira
eliel.teotonio@gmail.com
