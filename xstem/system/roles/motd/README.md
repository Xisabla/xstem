motd
=========

Configure machine motd

Requirements
------------

/

Role Variables
--------------

### General variables

| **Name** | **Description** | **Default** |
|----------|-----------------|-------------|
| `motd_template` | Template file to use for motd configuration | `motd_default.j2` |

Dependencies
------------

/

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - { role: motd }

```

License
-------

MIT

Author Information
------------------

Gautier Miquet <xisabla.dev@gmail.com>
