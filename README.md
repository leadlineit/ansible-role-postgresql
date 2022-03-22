# Ansible Role for PostgreSQL Server 14

![Build Status](https://github.com/leadlineit/ansible-role-postgresql/actions/workflows/ansible-galaxy-ci.yml/badge.svg)

[![role](https://img.shields.io/badge/Galaxy-leadlineit.postgresql-48C9B0.svg)](https://galaxy.ansible.com/leadlineit/postgresql/)

This role helps to install and configure PostgreSQL Server 14 to Debian (buster/bullseye).

Requirements
------------

This role requires Ansible 2.9 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
    pgsql_data_dir: /path/to/psql/data
    pgsql_listen_addresses: 10.0.0.1, localhost, *
    pgsql_listen_port: 7654
    pgsql_auth_method: md5
```

Variables 'psql_data_dir', 'psql_listen_addresses' and 'psql_listen_port' are optional.
Default values for optional variables:

```yaml
    pgsql_data_dir: /var/lib/postgresql/14/main
    pgsql_listen_addresses: localhost
    pgsql_listen_port: 5432
    pgsql_auth_method: peer
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: leadlineit.postgresql, tags: postgresql }
```

License
-------

MIT

Author Information
------------------

This role was created by Artem Kasianchuk.
