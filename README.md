TeamCity Agent
=========

[![Build Status](https://travis-ci.org/matisku/ansible-teamcity-agent.svg?branch=master)](https://travis-ci.org/matisku/ansible-teamcity-agent)

This role will install and configure TeamCity Agent for TeamCity Server - CI tool from Jetbrains.
Feel free to use it along with my TeamCity Server role - [matisku.teamcity-server](https://github.com/matisku/ansible-teamcity-server).

## Requirements
1. `teamcity-server` - TeamCity Server
2. [ansiblebit.oracle-java](https://github.com/ansiblebit/oracle-java) - Java is required on TeamCity Agent

## Role Variables
| Variable name               | Default value      | Description                |
|-----------------------------|--------------------|----------------------------|
| teamcity_agent_server_url   |  `localhost`       | TeamCity Server URL        |
| teamcity_agent_server_port  |  `8111`            | TeamCity Server Port       |
| teamcity_agent_install_dir  |  `/opt/buildAgent` | TeamCity Agent Install Dir |
| teamcity_server_user_name   | `teamcity`         | Teamcity Adminin User      |
| teamcity_server_user_passwd | `teamcity`         | Teamcity Admin Password    |

## Dependencies
This role depends on `java` role.

## Example Playbook
Example playbook:

```yaml
- hosts: teamcity-agent
  roles:
    - matisku.teamcity-agent
```

## Author Information
This role was created by Mateusz Trojak for [Brainly](http://www.brainly.com).
We are using this role for company CI automation with easy scaling if needed.

## License
Copyright © 2017-2018 Mateusz Trojak. See LICENSE for details.
