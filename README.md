# k3s-server Ansible role

An Ansible role for ensuring the configuration of a master [K3s](https://k3s.io/) server node.

## Requirements

Requires Docker installed.

The role installs on Centos 7, Alpine 3.11 and Ubuntu bionic.

## Role Variables

| Variable                | Required | Default      | Choices                   | Comments                                 |
|-------------------------|----------|--------------|---------------------------|------------------------------------------|
| default_retries         | yes      | 60           | Integer value             | default number of retries                |
| default_delay           | yes      | 60           | Integer value             | default delay in seconds between retriies|
| k3s_version             | yes      | v1.17.5+k3s1 | matches release tag       | k3s version to install                   |

## Example Playbook

An example can be found used in my Hands-on DevOps course's [master-playbook.yml](https://github.com/nemonik/hands-on-DevOps/blob/master/ansible/master-playbook.yml).

```
- hosts: masters
  remote_user: vagrant
  roles:
    - k3s-server
```

For more information see the [Hands-on DevOps class](https://github.com/nemonik/hands-on-DevOp) project.

## License

3-Clause BSD License

## Author Information

Michael Joseph Walsh <mjwalsh@nemonik.com>
