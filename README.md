# Ansible Semantic Hostname

[![Ansible Role](https://img.shields.io/ansible/role/4378.svg)](https://galaxy.ansible.com/detail#/role/4378)
[![Build Status](https://travis-ci.org/shrikeh/ansible-semantic-hostname.svg)](https://travis-ci.org/shrikeh/ansible-semantic-hostname)
[![GitHub Stars](https://img.shields.io/github/stars/shrikeh/ansible-semantic-hostname.svg)][github]

Set up a [semantic hostname][semantic_hostname] for a host.


## Example playbook
```YAML
- hosts: all
  vars:
    # Override the RedHat short code from 'rhel' to 'rh'
    semantic_hostname_os_code_redhat: 'rh'
- hosts: redhat
    # Set the hostnames to use the semantic_hostname
    # If you don't set this to true, the role will not explicitly set the hostname
  vars:
    semantic_hostname_set: yes
  roles:
    - { role: shrikeh.semantic-hostname }

```
## License
-------

[MIT][licence]

## Author Information
------------------
Contact me on Twitter @[barney_hanlon][twitter]

[semantic_hostname]: https://github.com/semantic-hostnames/semantic-hostnames "Convention for Semantic Hostnames (CSH)"
[licence]: https://raw.githubusercontent.com/shrikeh/ansible-semantic-hostname/master/LICENSE
[twitter]: https://twitter.com/barney_hanlon "Link to my Twitter page"
