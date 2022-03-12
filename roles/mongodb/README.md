# ericsysmin.databases.mongodb

Ansible role that can install mongodb server and/or mongodb client.

## Role Variables

mongodb_install_service: true
mongodb_install_client: true
mongodb_ver: 4.4
mongodb_repository: `please see vars/`

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: ericsysmin.databases.mongodb
      mongodb_install_service: true
      mongodb_ver: 4.4
```

## License

MIT

## Author Information

Eric Anderson
[ericsysmin.com](http://ericsysmin.com)
