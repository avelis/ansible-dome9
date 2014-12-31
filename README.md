ansible-dome9
=============

This ansible role installs and configures the Dome9 Security Agent (Security Monitor Daemon)

## Requirements

This role requires Ansible 1.4 higher and platforms listed in the metadata file.

## Role Variables

The variables that can be passed to this role and a brief description about them are as follows

    dome9_pairkey: pc6bd5cab6d944f588c # Pair key with Dome9 service
    dome9_enabled: yes                 # The role is enabled
    dome9_secgroups: [ 'Default' ]     # Security groups specific for a Dome9 account

## Examples

### Paramaterized Role

    ---
    - hosts: all
      roles:
        - { role: dome9, dome9_pairkey: pc6bd5cab6d944f588c }

### Vars

    ---
    - hosts: all
      vars:
        dome9_pairkey: pc6bd5cab6d944f588c
      roles:
        - dome9

### Group vars

#### group_vars/production

    ---
    dome9_pairkey: pc6bd5cab6d944f588c

#### site.yml

    ---
    - hosts: all
      roles:
        - dome9