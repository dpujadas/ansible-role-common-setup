common-setup
============

This role performs some common setup steps on Ubuntu server

Role Variables
--------------

- `common_setup_full_upgrade`: Perform apt upgrade or not (default: False)
- `common_setup_hostname`: New host name (Ex: 'test-server')
- `common_setup_timezone`: New time zone (Ex: 'Europe/Madrid')
- `common_setup_ntp`: Setup ntp or not, Ubuntu 16.04 has systemd-timesyncd enabled by default (default: False)

Example Playbook
----------------

    - hosts: servers
      roles:
        - {
          role: common-setup,
          common_setup_hostname: 'test-server',
          common_setup_timezone, 'Europe/Madrid'
        }

License
-------

MIT

[![Build Status](https://travis-ci.org/dpujadas/ansible-role-common-setup.svg?branch=master)](https://travis-ci.org/dpujadas/ansible-role-common-setup)
