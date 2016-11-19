TeamCity Agent
=========

[![Build Status](https://travis-ci.org/matisku/ansible-teamcity-agent.svg?branch=master)](https://travis-ci.org/matisku/ansible-teamcity-agent)

This role will install and configure TeamCity Agent for TeamCity Server - CI tool from Jetbrains.
Feel free to use it along with my TeamCity Server role - [matisku.teamcity-server](https://github.com/matisku/ansible-teamcity-server).

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
- hosts: teamcity-agent
  roles:
    - matisku.teamcity-agent
```

## Author Information
----------------

This role was created in 2016 by Mateusz Trojak for [Brainly](http://www.brainly.com).
We are using this role for company CI automation with easy failover mechanism.
