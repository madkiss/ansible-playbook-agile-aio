Ansible Role for NTP
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-ntp.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-ntp)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-ntp.svg)](https://github.com/pantarei/ansible-role-ntp)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-ntp.svg)](https://github.com/pantarei/ansible-role-ntp/blob/master/LICENSE)

Ansible Role for NTP Management.

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
<td>ntp_driftfile</td>
<td>yes</td>
<td>/var/lib/ntp/ntp.drift</td>
<td></td>
<td>Specify the name and path of the frequency file.</td>
</tr>
<tr class="even">
<td>ntp_filegen</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Configures setting of generation file set name.</td>
</tr>
<tr class="odd">
<td>ntp_restrict</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Access control configuration; see <a href="http://support.ntp.org/bin/view/Support/AccessRestrictions">web page</a> for details.</td>
</tr>
<tr class="even">
<td>ntp_server</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Specify one or more NTP servers.</td>
</tr>
<tr class="odd">
<td>ntp_statistics</td>
<td>no</td>
<td>loopstats peerstats clockstats</td>
<td></td>
<td>Enables writing of statistics records.</td>
</tr>
<tr class="even">
<td>ntp_statsdir</td>
<td>no</td>
<td>/var/log/ntpstats</td>
<td></td>
<td>Specify the directory path for files created by the statistics facility.</td>
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
        - role: hswong3i.ntp

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-ntp/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

