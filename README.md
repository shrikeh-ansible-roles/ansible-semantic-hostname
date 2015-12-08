# Ansible Semantic Hostname

[![Ansible Role](https://img.shields.io/ansible/role/4378.svg)][galaxy]
[![Build Status](https://travis-ci.org/shrikeh/ansible-semantic-hostname.svg)][build]
[![GitHub Stars](https://img.shields.io/github/stars/shrikeh/ansible-semantic-hostname.svg)][stargazers]
[![License](https://img.shields.io/github/license/shrikeh/ansible-semantic-hostname.svg)][licence]

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
[galaxy]: https://galaxy.ansible.com/detail#/role/5824 "This role on Ansible Galaxy"
[build]: https://travis-ci.org/shrikeh-ansible-roles/ansible-rsyslog8 "Build status"
[stargazers]: https://github.com/shrikeh-ansible-roles/ansible-rsyslog8 "Stargazers on GitHub"
