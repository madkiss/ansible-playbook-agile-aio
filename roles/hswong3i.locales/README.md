Ansible Role for Locale
=======================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-locales.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-locales)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-locales.svg)](https://github.com/pantarei/ansible-role-locales)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-locales.svg)](https://github.com/pantarei/ansible-role-locales/blob/master/LICENSE)

Ansible Role for Locale Management.

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
<td>locales_lang</td>
<td>yes</td>
<td>en_US.UTF-8</td>
<td></td>
<td>Provides default value for LC_* variables that have not been explicitly set.</td>
</tr>
<tr class="even">
<td>locales_language</td>
<td>no</td>
<td></td>
<td></td>
<td>Provides fallback locales, if a translation for the preferred locale is unavailable, another from a similar locale will be used instead of the default.</td>
</tr>
<tr class="odd">
<td>locales_lc</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-locales/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>All <code>LC_*</code> variables.</td>
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
        - role: hswong3i.locales
          locales_lang: "en_US.UTF-8"

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-locales/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

