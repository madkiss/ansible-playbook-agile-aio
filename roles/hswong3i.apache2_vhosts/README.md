Ansible Role for Apache2 VirtualHost
====================================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-apache2-vhosts.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-apache2-vhosts)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-apache2-vhosts.svg)](https://github.com/pantarei/ansible-role-apache2-vhosts)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-apache2-vhosts.svg)](https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/LICENSE)

Ansible Role for Apache2 VirtualHost Management.

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
<td>apache2_vhosts_base</td>
<td>yes</td>
<td>{{ apache2_vhosts_home }}</td>
<td></td>
<td>VirtualHost base directory.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_custom_log</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Sets filename and format of log file.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_document_root</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Directory that forms the main document tree visible from the web.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_error_log</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Location where the server will log errors.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_gid</td>
<td>no</td>
<td></td>
<td></td>
<td>Specifying the GID for shared storage. NOTE: This value should only be set once before deploying and then never changed.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_handler_php</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Forces all matching files with <code>\.php$</code> to be processed by a handler.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_hash_salt</td>
<td>yes</td>
<td></td>
<td></td>
<td>Specific password hash salt for sha512.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_home</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Location for the virtual host user home directory.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_http_port</td>
<td>yes</td>
<td>80</td>
<td></td>
<td>Apache2 VirtualHost HTTP port.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_https_port</td>
<td>yes</td>
<td>443</td>
<td></td>
<td>Apache2 VirtualHost HTTPS port.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_id</td>
<td>yes</td>
<td></td>
<td></td>
<td>Unique ID for virtual host shared among other services.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_pass</td>
<td>yes</td>
<td></td>
<td></td>
<td>Password for virtual host user.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_proxy_pass</td>
<td>no</td>
<td></td>
<td></td>
<td>Maps remote servers into the local server URL-space.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_proxy_pass_reverse</td>
<td>no</td>
<td></td>
<td></td>
<td>Adjusts the URL in HTTP response headers sent from a reverse proxied server.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_proxy_preserve_host</td>
<td>yes</td>
<td></td>
<td><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td>Use incoming Host HTTP request header for proxy request.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_proxy_request</td>
<td>no</td>
<td></td>
<td><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td>Enables forward (standard) proxy requests.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_proxy_via</td>
<td>yes</td>
<td></td>
<td><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td>Information provided in the Via HTTP response header for proxied requests.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_redirect</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Sends an external redirect asking the client to fetch a different URL.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_server_admin</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Email address that the server includes in error messages sent to the client.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_server_alias</td>
<td>no</td>
<td><code>[]</code></td>
<td><ul>
<li><code>list</code></li>
<li><code>[]</code></li>
</ul></td>
<td>Alternate names for a host used when matching requests to name-virtual hosts.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_server_name</td>
<td>yes</td>
<td></td>
<td></td>
<td>Hostname and port that the server uses to identify itself.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_ssl_certificate_chain_file</td>
<td>no</td>
<td></td>
<td></td>
<td>File of PEM-encoded Server CA Certificates.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_ssl_certificate_file</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Server PEM-encoded X.509 certificate data file.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_ssl_certificate_key_file</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Server PEM-encoded private key file.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_ssl_engine</td>
<td>no</td>
<td></td>
<td><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td>SSL Engine Operation Switch.</td>
</tr>
<tr class="even">
<td>apache2_vhosts_uid</td>
<td>no</td>
<td></td>
<td></td>
<td>Specifying the UID for shared storage. NOTE: This value should only be set once before deploying and then never changed.</td>
</tr>
<tr class="odd">
<td>apache2_vhosts_user</td>
<td>yes</td>
<td></td>
<td></td>
<td>Username for virtual host user.</td>
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
        - role: hswong3i.apache2_vhosts
          apache2_vhosts_hash_salt: "wi6Eereiwae7phae"
          apache2_vhosts_id: "example"
          apache2_vhosts_pass: "xaivoo9Z"
          apache2_vhosts_server_name: "example.com"
          apache2_vhosts_user: "example" 

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-apache2-vhosts/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

