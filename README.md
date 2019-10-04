# ROLE NTP

[![GitHub](https://img.shields.io/github/license/adfinis-sygroup/ansible-role-ntp.svg?style=flat-square)](https://github.com/adfinis-sygroup/ansible-role-ntp/blob/master/LICENSE)
[![Travis (.org)](https://img.shields.io/travis/adfinis-sygroup/ansible-role-ntp.svg?style=flat-square)](https://travis-ci.org/adfinis-sygroup/ansible-role-ntp)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-adfinis--sygroup.ntp-660198.svg?style=flat-square)](https://galaxy.ansible.com/adfinis-sygroup/ntp)

This role configures and manages the NTP daemon (ntpd).

## Requirements

This role has no additional requirements.

## Role Variables

The following defaults variables can be configured:

``` yaml
# a list of ntp servers
ntp_servers:
  - 0.pool.ntp.org
  - 1.pool.ntp.org
  - 2.pool.ntp.org
  - 3.pool.ntp.org

# NTP clients that are allowed to query this server. If non-empty, this host is
# assumed to be an NTP server itself.
#
# Example:
#
#ntp_clients:
#  - ip4addr: 1.2.3.0
#    ip4mask: 255.255.255.0
#  - ip4addr: 4.3.2.64
#    ip4mask: 255.255.255.240
ntp_clients: []
```

For a list OS related variables that usually don't need to be customized have a
look at the vars/ directory.

## Dependencies

This role has no additional dependencies.

## Example Playbook

Below example shows how the role can be integrated into a playbook using
external vars:

``` yaml
- hosts: servers
  roles:
    - { role: adfinis-sygroup.ntp }
```

## License

[GPL-3.0](https://github.com/adfinis-sygroup/ansible-role-ntp/blob/master/LICENSE)

## Author Information

ntp role was written by:

-   Adfinis SyGroup AG \| [Website](https://www.adfinis-sygroup.ch/) \|
    [Twitter](https://twitter.com/adfinissygroup) \|
    [GitHub](https://github.com/adfinis-sygroup)
