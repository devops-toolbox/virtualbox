Role Name
=========

virtualbox

[![Build Status](https://travis-ci.org/cmihai-ansible/virtualbox.svg?branch=master)](https://travis-ci.org/cmihai-ansible/virtualbox)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/devopstoolbox.virtualbox](https://galaxy.ansible.com/devopstoolbox.virtualbox)

```bash
ansible-galaxy install devopstoolbox.virtualbox
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
virtualbox_remove_packages: true
virtualbox_enable_service: true
virtualbox_enable_selinux: true
virtualbox_firewall_configure: true
virtualbox_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install virtualbox on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: virtualbox is configured
      import_role:
        name: devopstoolbox.virtualbox
      vars:
        virtualbox_remove_packages: true
        virtualbox_enable_service: true
        virtualbox_firewall_configure: true
        virtualbox_firewall_rules:
          - service:
      tags: virtualbox
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai)
