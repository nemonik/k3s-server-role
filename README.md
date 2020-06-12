# k3s-server

Ansible for ensuring the configuration of a master K3s server node.

Used in my [Hands-on DevOps course](https://github.com/nemonik/hands-on-DevOp)

## Requirements

Requires Docker.

## Role Variables

| Variable                | Required | Default      | Choices                   | Comments                                 |
|-------------------------|----------|--------------|---------------------------|------------------------------------------|
| default_retries         | yes      | 60           | Integer value             | default number of retries                |
| default_delay           | yes      | 60           | Integer value             | default delay in seconds between retriies|
| k3s_version             | yes      | v1.17.5+k3s1 | matches release tag       | k3s version to install                   |

## Example Playbook

```
- hosts: masters
  remote_user: vagrant
  roles:
    - k3s-server
```

## License

3-Clause BSD License

## Author Information

Michael Joseph Walsh <mjwalsh@nemonik.com>
