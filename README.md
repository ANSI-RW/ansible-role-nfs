# Ansible Role: NFS

[![Build Status](https://img.shields.io/travis/rwanyoike/ansible-role-nfs.svg)](https://travis-ci.org/rwanyoike/ansible-role-nfs) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/rwanyoike/ansible-role-nfs/master/LICENSE)

Installs and configures NFS on RHEL/CentOS ~~or Debian/Ubuntu~~.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
nfs_exports: []
```

A list of exports which will be placed in the `/etc/exports` file.

```yaml
nfs_exports_template_path: exports.j2
```

The exports file to be copied. Defaults the the simple template inside `templates/exports.j2`. This path should be relative to the directory from which you run your playbook.

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
