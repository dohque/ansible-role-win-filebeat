Ansible Role: win_filebeat
===============================

[![Build Status](https://travis-ci.org/dohque/ansible-role-win-filebeat.svg?branch=release)](https://travis-ci.org/dohque/ansible-role-win-filebeat)

An Ansible Role that installs Filebeat on Windows.


Requirements
------------

Windows box should be prepared and configured to be accessible by Ansible.

<http://docs.ansible.com/ansible/intro_windows.html#windows-system-prep>


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
filebeat_version: 1.2.3
```

Filebeat version to install.

```yaml
filebeat_config_dir: "C:/ProgramData/filebeat/conf.d"
```

Directory where to look for prospector configurations.

```yaml
filebeat_elastic_search_hosts: [ "localhost:9200" ]
```

List of Elasticsearch hosts filebeat will connect to.

```yaml
filebeat_logging_level: error
```

Logging level for filebeat logs.

Dependencies
------------

  None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: dohque.win_filebeat }
```

Contributions
-------------

I will really appreciate any feedback and contributions. Feel free to contact me.

License
-------

MIT

Author Information
------------------

This role was created in 2016 by Ruslan Pilin.
