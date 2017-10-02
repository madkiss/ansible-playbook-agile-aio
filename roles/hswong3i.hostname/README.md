Ansible Role for Hostname
=========================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-hostname.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-hostname)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-hostname.svg)](https://github.com/pantarei/ansible-role-hostname)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-hostname.svg)](https://github.com/pantarei/ansible-role-hostname/blob/master/LICENSE)

Ansible Role for Hostname Management.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04 LTS and Ubuntu Server 16.04 LTS.

Note that this role will setup the target hostname with [Ansible Magic Variables](http://docs.ansible.com/ansible/playbooks_variables.html#magic-variables-and-how-to-access-information-about-other-hosts) `ansible_default_ipv4.address`, `inventory_hostname` and `inventory_hostname_short`, so it will depend on your Ansible inventory file which hosts should defined with their FQDN, e.g.

    foo.bar.com
    baz.bar.com     ansible_host=xxx.xxx.xxx.xxx

Moreover, this role will also generate the `/etc/hosts` based on all hosts that are in scope for the current play.

Role Variables
--------------

No additional role variables.

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: hswong3i.hostname

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-hostname/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

