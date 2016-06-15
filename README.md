JBoss Fuse on EAP
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.jboss--fuse-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/jboss-fuse)

Install JBoss Fuse on EAP.

Requirements
------------

Fuse installation JAR file must be downloaded and placed in `files` or available for download at `jboss_fuse_jar_file_url`.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `jboss_fuse_jar_file` | `fuse-eap-installer-6.2.1.redhat-084.jar` |  |
| `jboss_fuse_jar_file_url` | `[undefined]` | When defined, download the installer jar file from this URL instead of coping from the control node. |
| `jboss_fuse_install_dir` | `/var/tmp` | Where the jar file will be downloaded/copied to. |


Dependencies
------------

- `samdoran.java`
- `samdoran.redhat-subscription`

Example Playbook
----------------

    - hosts: fuse
      roles:
         - samdoran.redhat-subscription
         - samdoran.java
         - samdoran.jboss-eap
         - samdoran.jboss-fuse

License
-------

MIT
