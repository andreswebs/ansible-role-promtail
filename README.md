# ansible-role-promtail

Ansible role to install promtail.

## Requirements

The `jq` program must be installed on the host. See the
[jq web page](https://stedolan.github.io/jq/) to install.

## Install

```sh
ansible-galaxy install andreswebs.promtail
```

## Role Variables

- `promtail_loki_url`: Set the Loki URL in the format `<protocol>://<host>:<port>`.
  The default value is `http://localhost:3100`.

## Example Playbook

```yaml
---
- hosts: servers
  roles:
    - role: andreswebs.promtail
      vars:
        promtail_loki_url: http://loki.example.com:3100
```

## Authors

**Andre Silva** [@andreswebs](https://github.com/andreswebs)

## License

This project is licensed under the [Unlicense](UNLICENSE.md).
