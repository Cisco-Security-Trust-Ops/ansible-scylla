# Ansible Role: ScyllaDB

An Ansible Role that installs ScyllaDB on RHEL/CentOS

## Requirements

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    scylladb_repo_url: ""

The repository to use when installing ScyllaDB.  ScyllaDB repos must be obtained from https://www.scylladb.com/download/open-source/#binary

    scylladb_version: ""

The version of the file.  If not given, the version is the point is the present package

    scylladb_cluster_name: ""

Set the selected cluster_name for the cluster. The default cluster name is 'Test Cluster'. The Cluster name of an existing cluster can't be changed

    scylladb_developer_mode: "true"

For test environments set scylladb_developer_mode to "true" to prevent Scylla from performing operating system and hardware configuration checks which could fail the startup of the node. For production the value has to be changed to "false".

    scylladb_state: "restarted"

Restart handler variable whether the service should be restarted when handler is called.

    scylladb_enabled: "yes"

Restart handler variable whether the service should start on boot. Default is set to "enabled == yes"
    
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
