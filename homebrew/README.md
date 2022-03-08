Role Name
=========

Ansible role to install homebrew on Ubuntu 20.x

Requirements
------------

Vagrant for local testing & development.

Role Variables
--------------

| Variable                    | Type   | Description                                  |
| --------------------------- |:------:|:---------------------------------------------:
| ansible_ssh_port            | int    | Speicify ssh port for the nodes (default 22) |
| curl_state_pkg_latest       | str    | Specify curl version (latest, present        |
| update_pkg_manager          | str    | Update package manager  (yes, no)            |    


Example Playbook
----------------

<pre>
  - hosts: all
  roles:
    - role: homebrew
</pre>

License
-------

MIT

Author Information
------------------

Mustafa Saadi (0p0inter)
