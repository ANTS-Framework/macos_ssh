macOS ssh
=========

[![Build Status](https://travis-ci.org/ANTS-Framework/macos_ssh.svg?branch=master)](https://travis-ci.org/ANTS-Framework/macos_ssh)

This role is used to enable remote login (SSH) for admins or for everyone.

Role Variables
--------------
```yml
# Enable or disable ssh
macos_ssh__ssh_enabled: True
# Enable ssh for admin group or for everyone
macos_ssh__ssh_access_everyone: False
```

Example Playbook
----------------

```yml
# Clients with ssh enabled for admin
# This is the default, so we do not need to change a variable.
- hosts: ssh_admin
  roles:
  - role: macos_ssh

# Clients with ssh disabled
- hosts: ssh_admin
  vars:
    - macos_ssh__ssh_enabled: False
  roles:
  - role: macos_ssh

# Clients with ssh enabled for everyone
- hosts: ssh_admin
  vars:
    - macos_ssh__ssh_access_everyone: True
  roles:
  - role: macos_ssh
```

License
-------

GPLv3

Author Information
------------------

Part of the [ANTS Framework](https://ants-framework.github.io/)
