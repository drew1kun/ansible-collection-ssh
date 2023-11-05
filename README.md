# Ansible Collection - drew1kun.ssh

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][collection-badge]][galaxy-link]

This collection contains Ansible roles for generating SSH keys and configuring SSH Certificate Authority (CA) based infrastructure on Mac and Linux hosts.

The roles included:

  - `drew1kun.ssh.keygen` ([doc](https://github.com/drew1kun/ansible-collection-ssh/blob/main/roles/keygen/README.md))
  - `drew1kun.ssh.ca_host` ([doc](https://github.com/drew1kun/ansible-collection-ssh/blob/main/roles/ca_host/README.md))
  - `drew1kun.ssh.ca_user` ([doc](https://github.com/drew1kun/ansible-collection-ssh/blob/main/roles/ca_user/README.md))

## Installation

Install via Ansible Galaxy:

```
ansible-galaxy collection install drew1kun.ssh
```

Or include this collection in your playbook's `requirements.yml` file:

```yaml
---
collections:
  - name: drew1kun.ssh
```
And run:
```
ansible-galaxy install -r requirements.yml
```

## Usage

Example of the play:

```yaml
- hosts: localhost
  connection: local
  roles:
    - drew1kun.ssh.keygen
    - drew1kun.ssh.ca_host
    - drew1kun.ssh.ca_user

```

## License

[MIT][mit-link]

## Author Information

Andrew Shagayev | [e-mail](mailto:drew-kun@protonmail.com)

[collection-badge]: https://img.shields.io/badge/collection-drew1kun.ssh-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew1kun/ssh
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew1kun/ansible-collection-ssh/main/LICENSE
