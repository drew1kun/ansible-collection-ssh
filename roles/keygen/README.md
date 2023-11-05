Ansible role: ssh.keygen
====

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Collection][collection-badge]][galaxy-link]

Cross-platform ansible role for generating SSH keypairs. 

The role is the part of collection for configruing SSH authentication using Certificate Chain of Trust.

Requirements
----

NOTE: Role requires Fact Gathering by ansible!

One of the following OS (or deriviatives):

 - Debian
 - CentOS
 - MacOS
 - FreeBSD

NOTE: In order to manage multiple users, the sshd on the managed host must allow enough sessions.
Paramiko module spits out the Warning and Error.
Warning: No handlers could be found for logger "paramiko.transport"
Error: 'Failed to open session'
Solution: set 'MaxSessions 4' (or higher)in sshd_config before provisioning

Role Variables
----


Please review:

 - [`defaults/main.yml`](defaults/main.yml)
 - [`defaults/linux.yml`](vars/linux.yml)
 - [`defaults/freebsd.yml`](vars/freebsd.yml)
 - [`defaults/darwin.yml`](vars/darwin.yml)
 
Dependencies
----

None

Example Playbook
----

Install collection:

    ansible-galaxy collection install drew1kun.ssh

Include role in the playbook:

```yaml
- hosts: hosts
  gather_facts: yes
  roles:
    - role: drew1kun.ssh.keygen
```

License
----

[MIT][mit-link]

Author Information
----

Andrew Shagayev | [e-mail](mailto:drewshg@gmail.com)

[collection-badge]:https://img.shields.io/badge/collection-drew1kun.ssh-green.svg

[galaxy-link]: https://galaxy.ansible.com/drew1kun/ssh/

[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg

[mit-link]: https://raw.githubusercontent.com/drew1kun/ansible-collection-ssh/master/LICENSE