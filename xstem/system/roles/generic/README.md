generic
=========

Perform basic and generic actions

Requirements
------------

/

Role Variables
--------------

| **Name** | **Description** | **Default** |
|----------|-----------------|-------------|
| `pre_generic_packages` | Packages that must be installed before any other package | `[ epel-release ]` |
| `generic_packages` | Very basic packages that must be installed on all machines | `[ glibc-common, glibc-langpack-en ]` |
| `generic_packages_extra` | Extra packages to install on all machines | `[]` |
| `generic_timezone` | Timezone to set | `"UTC"` |

Dependencies
------------

/

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - { role: generic }

```

License
-------

MIT

Author Information
------------------

Gautier Miquet <xisabla.dev@gmail.com>
