TeamCity Agent
=========

This role will install and configure TemCity Agent - CI tool from Jetbrains.

Requirements
------------

1. 'teamcity-server' - TeamCity Server

Role Variables
--------------

| Variable name              | Default value    | Description                      |
|----------------------------|------------------|----------------------------------|
| teamcity_agent_server_url  |  localhost       | TeamCity Server URL              |
| teamcity_agent_server_port |  8111            | TeamCity Server Port             |
| teamcity_agent_install_dir |  /opt/buildAgent | TeamCity Agent Install Dir       |

Dependencies
------------

This role depends on 'java' and 'docker' role.

Example Playbook
----------------

Example playbook:

```yaml
- hosts: agents
  roles:
    - teamcity-agent
```
