# Ansible Collection - ericsysmin.databases

Ansible collection that holds roles, that can be used to configure common database services.

## Roles

| Role       | Build Status                                                                                                                                                                                                                                         | Documentation                                                                                                    |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| pgadmin4   | [![ericsysmin.databases.pgadmin4](https://github.com/ericsysmin/ansible-collection-databases/actions/workflows/pgadmin4.yml/badge.svg?branch=main)](https://github.com/ericsysmin/ansible-collection-databases/actions/workflows/pgadmin4.yml)       | [Documentation](https://github.com/ericsysmin/ansible-collection-databases/blob/main/roles/pgadmin4/readme.md)   |
| postgresql | [![ericsysmin.databases.postgresql](https://github.com/ericsysmin/ansible-collection-databases/actions/workflows/postgresql.yml/badge.svg?branch=main)](https://github.com/ericsysmin/ansible-collection-databases/actions/workflows/postgresql.yml) | [Documentation](https://github.com/ericsysmin/ansible-collection-databases/blob/main/roles/postgresql/readme.md) |
| mongodb    | [![ericsysmin.databases.mongodb](https://github.com/ericsysmin/ansible-collection-databases/actions/workflows/mongodb.yml/badge.svg?branch=main)](https://github.com/ericsysmin/ansible-collection-databases/actions/workflows/mongodb.yml)          | [Documentation](https://github.com/ericsysmin/ansible-collection-databases/blob/main/roles/mongodb/readme.md)    |

## Usage

You can find specific to each role within the "Documentation" link for each role. However, most should be in this format.

```yaml
---
- hosts: localhost
  connection: local
  tasks:
    - name: Include role
      include_role:
        name: ericsysmin.databases.<role_name>
      vars:
        var1: value1
        var2: value2
```

## Testing

Testing is done through GitHub Actions, and can be tested locally as well. GitHub Actions can be located [here](https://github.com/ericsysmin/ansible-collection-databases/actions).
Each workflow pertains to a single role, and can be launched locally using the following command:

```bash
MOLECULE_COMMAND={{ matrix.molecule_distro.command }} \
MOLECULE_DISTRO={{ matrix.molecule_distro.distro }} \
molecule --debug test -s {{ matrix.collection_role }}
```

To decide on the `MOLECULE_COMMAND` value please refer to the `.github/workflow/{{ collection_role }}.yml` file as it will have the value for proper systemd services.
