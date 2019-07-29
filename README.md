Ansible Workstation Collection
==============================

[Ansible Galaxy Collection: Workstation](https://galaxy.ansible.com/crivetimihai/workstation):

- dotfiles
- profile
- packages

Tested on:
----------

- CentOS 7
- RHEL 8
- Fedora 30
- Ubuntu 18.04
- Debian 10

Example
-------

### Install the role:

```bash
pip install --upgrade mazer
mazer install crivetimihai.workstation
```


### playbook.yml example

```yaml
- name: setup a workstation environment
  hosts: all
  connection: local
  become: yes
  gather_facts: yes
  roles:
    - role: crivetimihai.workstation.dotfiles
```

