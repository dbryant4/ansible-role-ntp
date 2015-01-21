# NTP Role

[![Build
Status](https://travis-ci.org/dbryant4/ansible-role-ntp.svg?branch=master)](https://travis-ci.org/dbryant4/ansible-role-ntp)

## Description

This role manages the installation of NTP on a Raspberry Pi, although it
should be able to manage any other Debian based system. This role only
currently manages the NTP as a client.

## Provides

1. An NTP client

## Requires

1. Ansible 1.7 or higher
2. Raspberry Pi (possibly other Debian based systems)

## Variables
-  ntp_servers - Remote NTP servers which are used by the node to sync
   its time

### Changing Variable Values

To Change the value of variables, create a file in `host_vars/` or `group_vars/` or define variables in the playbook.

There are other options for changing variable values. See [Ansible
Variable
Documentation](http://docs.ansible.com/playbooks_variables.html) for
more ideas.

## Usage

Include this role in your plays and set varaibles as desired.

```yaml
---
  name: ntp
  hosts: my_host
  vars:
    ntp_servers:
      - ntp.server1
      - ntp.server2
  roles:
    - ntp
```

## Tests
This role includes Travis CI tests.
