Ansible Role: nvidia driver
=========

**Notice: Not tested yet**

Install nvidia driver on Ubuntu 16.04.
This role performs the followig tasks if a nvidia driver of specified version has not been installed:

- Copy config file to disable Nouveau
- Add apt repository
- Install nvidia driver of specified version

All the tasks need root privilege.

Requirements
------------

None.

Role Variables
--------------

Version of nvidia driver.

``` yaml
nvidia_driver_version: 375
```

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
- hosts: all
  vars_files:
      - vars/main.yml
  roles:
      - {role: nvidia_driver, become: yes}
```

License
-------

MIT

