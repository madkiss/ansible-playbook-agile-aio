Ansible Role for Apache2
========================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-apache2.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-apache2)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-apache2.svg)](https://github.com/pantarei/ansible-role-apache2)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-apache2.svg)](https://github.com/pantarei/ansible-role-apache2/blob/master/LICENSE)

Ansible Role for Apache2 Installation.

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
<td>apache2_http_port</td>
<td>yes</td>
<td>80</td>
<td></td>
<td>Apache2 HTTP listen port.</td>
</tr>
<tr class="even">
<td>apache2_https_port</td>
<td>yes</td>
<td>443</td>
<td></td>
<td>Apache2 HTTPS listen port.</td>
</tr>
<tr class="odd">
<td>apache2_log_level</td>
<td>yes</td>
<td>warn</td>
<td></td>
<td>LogLevel: Control the severity of messages logged to the error_log.</td>
</tr>
<tr class="even">
<td>apache2_module</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip enable module if <code>[]</code>, or pass <code>list</code> to <a href="http://docs.ansible.com/ansible/apache2_module_module.html">apache2_module module</a>.</td>
</tr>
<tr class="odd">
<td>apache2_timeout</td>
<td>yes</td>
<td>300</td>
<td></td>
<td>Timeout: The number of seconds before receives and sends time out.</td>
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
        - role: hswong3i.apache2

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-apache2/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

