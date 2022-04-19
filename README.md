OULibraries.aws
=========

A role that handles the installation and management of the AWS-packaged version of the `awscli` tool (version 2).

Requirements
------------

The `unzip` package is required to make use of the `unarchive` module, but it is installed by the role before the unarchive task is needed.

Role Variables
--------------

There are currently only two variables (located in `defaults/main.yml`). Because they are set by default, they should only occasionally need to be modified or overridden. The variables are:

`awscli_version: `                 - Rather than installing the most current version of the AWS-managed package
`awscli_clean_previous_versions: ` - By default, this value is set to false. If it is set to `true`, it will perform a task that will delete all previous version of the awscli located in `/usr/local/aws-cli/v2/`. It is recommended that this value only be set to true using the `--extra-vars` argument when running any associated playbooks. 

Dependencies
------------

This role does not depend on any other roles.

Example Playbook
----------------

    - hosts: all
      roles:
         - role: OULibraries.aws

License
-------

[MIT](https://github.com/OULibraries/ansible-role-centos7/blob/master/LICENSE)

Author Information
------------------

James Mitchell
