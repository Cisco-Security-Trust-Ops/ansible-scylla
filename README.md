# Ansible Role: ScyllaDB

An Ansible Role that installs ScyllaDB on RHEL/CentOS

## Requirements

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    scylladb_repo_url: ""

The repository to use when installing ScyllaDB.  ScyllaDB repos must be obtained from https://www.scylladb.com/download/open-source/#binary

    scylladb_version: ""

The version of the file.  If not given, the version is the point is the present package

## Dependencies

None.

## Example Playbook

    - hosts: scyalldb
      vars_files:
        - vars/main.yml
      roles:
        - { role: ansible-scylla }

*Inside `vars/main.yml`*:

    scylladb_repo_url: http://repositories.scylladb.com/scylla/repo/dfsdfadf-sdf/centos/scylladb-3.3.repo

## License

MIT / BSD
