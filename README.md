# Ansible Role: NFS

[![Build Status](https://img.shields.io/travis/thestarkenya/ansible-role-nfs.svg)](https://travis-ci.org/thestarkenya/ansible-role-nfs) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/thestarkenya/ansible-role-nfs/master/LICENSE)

Installs and configures NFS on RHEL/CentOS ~~or Debian/Ubuntu~~.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# Directories exported to NFS
nfs_exports: []
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers

  vars_files:
    - vars/main.yml

  roles:
    - role: ansible-role-nfs
```

Inside `vars/main.yml`:

```yaml
nfs_exports:
  - /home/public *(rw,sync,no_root_squash)

# ... etc ...
```

## License

MIT
