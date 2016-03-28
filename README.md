Ansible Role: NFS
=================

[![Build Status](https://img.shields.io/travis/ANSI-RW/ansible-role-nfs.svg)](https://travis-ci.org/ANSI-RW/ansible-role-nfs) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/ANSI-RW/ansible-role-nfs/master/LICENSE)

Installs and configures NFS on RHEL/CentOS or Debian/Ubuntu.

Requirements
------------

None

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# Directories exported to NFS
nfs_exports: []
# Enable service
nfs_enable_service: true
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers

  vars_files:
    - vars/main.yml

  roles:
    - { role: ANSI-RW.nfs }
```

Inside `vars/main.yml`:

```yaml
nfs_exports:
  - /mnt/public *(rw,sync,no_root_squash)

# ... etc ...
```

License
-------

MIT
