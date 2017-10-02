Ansible Role for UFW
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-ufw.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-ufw)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-ufw.svg)](https://github.com/pantarei/ansible-role-ufw)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-ufw.svg)](https://github.com/pantarei/ansible-role-ufw/blob/master/LICENSE)

Ansible Role for Ubuntu UFW Management.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04 LTS and Ubuntu Server 16.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ufw</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ufw/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Pass list to <a href="http://docs.ansible.com/ansible/ufw_module.html">ufw module</a>.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: hswong3i.ufw
          ufw:
            - { interface: "lo", direction: "in", rule: "allow" }
            - { from_ip: "224.0.0.0/4", rule: "allow" }
            - { from_ip: "10.0.0.0/8", rule: "allow" }
            - { from_ip: "172.16.0.0/12", rule: "allow" }
            - { from_ip: "192.168.0.0/16", rule: "allow" }
            - { to_port: "22", proto: "tcp", rule: "allow" }
            - { to_port: "1024:65535", proto: "tcp", rule: "allow" }
            - { direction: "incoming", policy: "deny" }
            - { direction: "outgoing", policy: "allow" }
            - { direction: "routed", policy: "allow" }
            - { logging: "on" }
            - { state: "enabled" }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-ufw/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

