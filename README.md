apache
=========

Install and configure Apache ansible role<br>
Available for Ubuntu 22.04 LTS<br>

    apache
    ├── README.md
    ├── tasks
    │  └── main.yml
    ├── templates
    │  ├── 000-default.conf.j2
    │  └── apache2.conf.j2
    └── vars
        └── main.yml

Requirements
------------

openssl

Role Variables
--------------

**apache:**<br>
&nbsp; **modules:**<br>
&nbsp; &nbsp; - *module name*<br>
&nbsp; &nbsp; ...<br>
&nbsp; **main_config_path:** *path to main config file*<br>
&nbsp; **main_config:** *main config file name*<br>
&nbsp; **virtual_host_config_path:** *path to virtual host config file*<br>
&nbsp; **virtual_host_config:** *virtual host config file name*<br>
&nbsp; **cert_directory:** *directory name for apache cert and key files*<br>
&nbsp; **virtual_hosts:** *virtual hosts list for* ***virtual_host_config*** *file*<br>
&nbsp; &nbsp; **- address:** *special address or group*<br>
&nbsp; &nbsp; &nbsp; **options:**<br>
&nbsp; &nbsp; &nbsp; &nbsp; **- name:** *option name*<br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; **value:** *option value*<br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ...<br>
&nbsp; &nbsp; &nbsp; ...<br>
&nbsp; &nbsp; *(all options are described in Apache documentation)*<br>
&nbsp; **directories:** *directories list in <Directory> tag of* ***main_config*** *file*<br>
&nbsp; &nbsp; **- path:** *path name*<br>
&nbsp; &nbsp; &nbsp; **options:**<br>
&nbsp; &nbsp; &nbsp; &nbsp; **- name:** *option name*<br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; **value:** *option value*<br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ...<br>
&nbsp; &nbsp; &nbsp; ...<br>
&nbsp; &nbsp; &nbsp; *(all options are described in Apache documentation)*<br>

Example Playbook
----------------

    - hosts: proxy_server
      roles:
         - apache
