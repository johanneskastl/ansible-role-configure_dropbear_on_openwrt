![Ansible Lint](https://github.com/johanneskastl/ansible-role-configure_dropbear_on_openwrt/workflows/Ansible%20Lint/badge.svg)

configure_dropbear_on_openwrt
=========

Configure the dropbear SSH server on OpenWRT

Requirements
------------

This role is intended to be used to configure a OpenWRT machine, so obviously you need one...

Role Variables
--------------

The role by default creates a configuration matching the default from a fresh installation of OpenWRT 22.03. The default values are kept, to not lock out a user by accident.

However, you can tweak the settings and disable root logins, root logins via password or password logins at all.

- `dropbear_port`: Port used by dropbear (default: `22` as an integer, not a string)
- `dropbear_allow_password_authentication`: Boolean that enables or disables password authentication in general (default: `true`)
- `dropbear_allow_root_login`:  Boolean that enables or disables root logins (default: `true`)
- `dropbear_allow_root_login_with_password`:  Boolean that enables or disables password-based login for root (default: `true`)

Additional variables:

- `dropbear_interface`: In case you want to limit which interface dropbear listens on, you can put the interface's name into this variable

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.configure_dropbear_on_openwrt'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
