# Ansible Role: NFS

[![Build Status](https://img.shields.io/travis/rwanyoike/ansible-role-nfs.svg)](https://travis-ci.org/rwanyoike/ansible-role-nfs) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/rwanyoike/ansible-role-nfs/master/LICENSE)

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
    - role: rwanyoike.nfs
```

Inside `vars/main.yml`:

```yaml
nfs_exports:
  - /home/public    *(rw,sync,no_root_squash)

# ... etc ...
```

## License

MIT

## Author Information

- This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
- This role was forked in 2015 by [Raymond Wanyoike](https://github.com/rwanyoike).
