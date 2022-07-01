# ericsysmin.databases.mongodb

Ansible role to install and configure MongoDB

## Role Variables

| Variable                | Default                                    | Description                        |
| ----------------------- | ------------------------------------------ | ---------------------------------- |
| mongodb_version         | 4.4                                        | Version of mongo to install        |
| mongodb_repository      | Please see vars/{{ ansible_distribution }} | Location of the MongoDB repository |
| mongodb_install_service | true                                       | Install MongoDB Server             |
| mongodb_install_client  | true                                       | Install MongoDB Client             |
| mongodb_config          | Please see defaults/main.yml               | Config file values                 |

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: mongodb-servers
  tasks:
    - name: Install mongodb
      ansible.builtin.include_role:
        name: ericsysmin.database.mongodb
      vars:
        mongodb_version: "5.0"
```

## License

BSD

## Author Information

Eric Anderson
