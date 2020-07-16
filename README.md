# Ansible amtega.mysql role

This is an [Ansible](http://www.ansible.com) role which install mysql community server whith replication option.

You can indicate the specific version by filling in the variable xxxx, but it will only be taken into account in CentOS / RHEL. The latest revision of the chosen minor version will be installed in Fedora.

Other considerations:
In the replica, the mysql server is assumed to be offline. By not supporting the master-data option in the mysql_db module, there is no way to guarantee the integrity of the replication if the master is online and receiving requests.

## Requirements

[Ansible 2.7+](http://docs.ansible.com/ansible/latest/intro_installation.html)

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

Because the internal network is used to interconnect the master and slave docker, the tests for the mysql sql installation and replication must be run separately.

Test mysql install over supported platforms:

```shell
cd amtega.mysql

molecule test
```

Test mysql replica master - slave:

```shell
cd amtega.mysql

molecule test --scenario-name replication
```

## License

Copyright (C) 2020 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- José Enrique Mourón Regueira
