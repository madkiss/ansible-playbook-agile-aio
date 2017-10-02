Ansible Role for MySQL VirtualHost
==================================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-mysql-vhosts.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-mysql-vhosts)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-mysql-vhosts.svg)](https://github.com/pantarei/ansible-role-mysql-vhosts)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-mysql-vhosts.svg)](https://github.com/pantarei/ansible-role-mysql-vhosts/blob/master/LICENSE)

Ansible Role for MySQL VirtualHost Management.

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
<td>mysql_vhosts_collation</td>
<td>yes</td>
<td>utf8mb4_general_ci</td>
<td></td>
<td>Pass value as <code>collation</code> to <a href="http://docs.ansible.com/ansible/mysql_db_module.html">mysql_db module</a>.</td>
</tr>
<tr class="even">
<td>mysql_vhosts_encoding</td>
<td>yes</td>
<td>utf8mb4</td>
<td></td>
<td>Pass value as <code>encoding</code> to <a href="http://docs.ansible.com/ansible/mysql_db_module.html">mysql_db module</a>.</td>
</tr>
<tr class="odd">
<td>mysql_vhosts_id</td>
<td>yes</td>
<td></td>
<td></td>
<td>Unique ID for virtual host shared among other services.</td>
</tr>
<tr class="even">
<td>mysql_vhosts_pass</td>
<td>yes</td>
<td></td>
<td></td>
<td>Pass value as <code>password</code> to <a href="http://docs.ansible.com/ansible/mysql_user_module.html">mysql_user module</a>.</td>
</tr>
<tr class="odd">
<td>mysql_vhosts_privs</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-mysql-user/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Pass list to <a href="http://docs.ansible.com/ansible/mysql_user_module.html">mysql_user module</a>.</td>
</tr>
<tr class="even">
<td>mysql_vhosts_user</td>
<td>yes</td>
<td></td>
<td></td>
<td>Pass value as <code>name</code> to <a href="http://docs.ansible.com/ansible/mysql_user_module.html">mysql_user module</a>.</td>
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
        - role: hswong3i.mysql_vhosts
          mysql_vhosts_id: "example"
          mysql_vhosts_pass: "xaivoo9Z"
          mysql_vhosts_user: "example"

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-mysql-vhosts/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

