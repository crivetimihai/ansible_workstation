Ansible Workstation Collection
==============================

[Ansible Galaxy Collection: Workstation](https://galaxy.ansible.com/crivetimihai/workstation):

- baseline: install baseline (epel for CentOS, python2-pip) as required by other roles
- dotfiles - download and link dotfiles from git repo
- flatpak - install and configure flatpaks
- baseline - baseline configuration (ex: sshd_config)
- micro - setup micro editor
- packages - install various packages
- pandoc - install pandoc
- pip - install various python modules from pip
- profile - setup profile, motd
- secure - secure the system (ex: sshd_config PermitRootLogin no)

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
ansible-galaxy collection install crivetimihai.workstation
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

### Running a single role:

```
ansible localhost -m include_role -a 'name=secure'
```

# See also:

- [Ansible Virtualization Collection](https://galaxy.ansible.com/crivetimihai/virtualization)
