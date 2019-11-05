# Dubzland: Hostname
[![Gitlab pipeline status (self-hosted)](https://img.shields.io/gitlab/pipeline/jdubz/dubzland-hostname?gitlab_url=https%3A%2F%2Fgit.dubzland.net)](https://git.dubzland.net/jdubz/dubzland-hostname/pipelines)

Updates the hostname (permanently) on a node.

## Requirements

Ansible version 2.9 or higher (for proper `hostname` module functionality).

## Role Variables

Available variables are listed below, along with their default values (see
    `defaults/main.yml` for more info):

### dubzland_hostname_fqdn

```yaml
dubzland_hostanme_fqdn: "{{ inventory_hostname }}"
```

Full hostname + domain (FQDN).

### dubzland_hostname_ip

```yaml
dubzland_hostname_ip: ""
```

IP address to associate with this host in `/etc/hosts` (leave blank to avoid
writing to the hosts file.

## Dependencies

None.

## Example Playbook

```yaml

- hosts: all
  roles:
    - role: dubzland-hostname
      vars:
        dubzland_hostname_fqdn: "host1.example.com"
```

## License

MIT

## Author

* [Josh Williams](https://codingprime.com)
