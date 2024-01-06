Ansible Role: apt
=========

A simple Ansible role to handle installing, removing and upgrading packages with apt.

Requirements
------------

None.

Role Variables
--------------

The following variables can be customized in `defaults/main.yml`:

```yaml
apt_cache_valid_time: 3600
```

Update the apt cache if it is older than the set value. This option is set in seconds.

```yaml
apt_packages_to_install: []
apt_packages_to_remove: []
```

Lists of packages to install (`apt_packages_to_install`) and to remove (`apt_packages_to_remove`).

```yaml
apt_upgrade: false
```

Control if the role should upgrade all upgradeable packages.

```yaml
apt_autoremove: false
apt_autoremove_purge: false
```

Control if the role should automatically remove all unneeded dependencies (`apt_autoremove`) and purge their configuration files (`apt_autoremove_purge`).


## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: obvionaoe.apt
```

License
-------

MIT

Author Information
------------------

This role was created in 2024 by [Luís Guimarães](https://obvionaoe.dev).
