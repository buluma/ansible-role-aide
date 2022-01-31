# [aide](#aide)

Install and configure aide on your system.

|GitHub|GitLab|Quality|Downloads|Version|
|------|------|-------|---------|-------|
|[![github](https://github.com/buluma/ansible-role-aide/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-aide/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-aide/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-aide)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/buluma/aide)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/buluma/aide)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-aide.svg)](https://github.com/buluma/ansible-role-aide/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.aide
```

The machine needs to be prepared. In CI this is done using `molecule/default/prepare.yml`:
```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: robertdebock.bootstrap
    - role: robertdebock.cron
    - role: robertdebock.postfix
      postfix_myhostname: "smtp.example.com"
      postfix_mydomain: "example.com"
      postfix_myorigin: "example.com"
```



## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-aide/blob/master/requirements.txt).

## [Status of used roles](#status-of-requirements)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-bootstrap)|
|[buluma.cron](https://galaxy.ansible.com/buluma/cron)|[![Build Status GitHub](https://github.com/buluma/ansible-role-cron/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-cron/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-cron/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-cron)|
|[robertdebock.postfix](https://galaxy.ansible.com/buluma/robertdebock.postfix)|[![Build Status GitHub](https://github.com/buluma/robertdebock.postfix/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/robertdebock.postfix/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/robertdebock.postfix/badges/master/pipeline.svg)](https://gitlab.com/buluma/robertdebock.postfix)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-aide/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|amazon|Candidate|
|el|8|
|debian|bullseye|
|fedora|all|
|opensuse|all|
|ubuntu|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

## [Exceptions](#exceptions)

Some roles can't run on a specific distribution or version. Here are some exceptions.

| variation                 | reason                 |
|---------------------------|------------------------|
| alpine | aide (missing): required by: world[aide] |
| debian:unstable | No package matching 'aide' is available |


If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-aide/issues)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[Michael Buluma](https://buluma.co.ke/)
