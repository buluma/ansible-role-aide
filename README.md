# [aide](#aide)

Install and configure aide on your system.

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-aide/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-aide/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-aide/badges/main/pipeline.svg)](https://gitlab.com/buluma/ansible-role-aide)|[![quality](https://img.shields.io/ansible/quality/57839)](https://galaxy.ansible.com/buluma/aide)|[![downloads](https://img.shields.io/ansible/role/d/57839)](https://galaxy.ansible.com/buluma/aide)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-aide.svg)](https://github.com/buluma/ansible-role-aide/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-aide.svg)](https://github.com/buluma/ansible-role-aide/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-aide.svg)](https://github.com/buluma/ansible-role-aide/pulls/)|

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
    - role: buluma.bootstrap
    - role: buluma.cron
    - role: buluma.postfix
      postfix_myhostname: "smtp.example.com"
      postfix_mydomain: "example.com"
      postfix_myorigin: "example.com"
```



## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-aide/blob/main/requirements.txt).

## [Status of used roles](#status-of-requirements)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-bootstrap/badges/main/pipeline.svg)](https://gitlab.com/buluma/ansible-role-bootstrap)|
|[buluma.cron](https://galaxy.ansible.com/buluma/cron)|[![Build Status GitHub](https://github.com/buluma/ansible-role-cron/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-cron/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-cron/badges/main/pipeline.svg)](https://gitlab.com/buluma/ansible-role-cron)|
|[buluma.postfix](https://galaxy.ansible.com/buluma/postfix)|[![Build Status GitHub](https://github.com/buluma/ansible-role-postfix/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-postfix/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-postfix/badges/main/pipeline.svg)](https://gitlab.com/buluma/ansible-role-postfix)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

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

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-aide/blob/main/CHANGELOG.md)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[Michael Buluma](https://buluma.github.io/)
