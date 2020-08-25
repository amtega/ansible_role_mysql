# Ansible amtega.mysql role

This is an [Ansible](http://www.ansible.com) role to install mysql community server whith replication option.

You can indicate the specific version by filling in the variable `mysql_version`, but it will only be taken into account in CentOS / RHEL. In Fedora will be installed the latest revision of the chosen minor version-

In the replica the mysql server is assumed to be offline because ansible mysql_db module does not support the master-data option, and there is no way to guarantee the integrity of the replication if the master is online and receiving requests.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - role: amtega.mysql
```

## Testing

Tests are based on [molecule with docker containers](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.mysql

molecule test --all
```

## License

Copyright (C) 2020 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- José Enrique Mourón Regueira
- Juan Antonio Valiño García
