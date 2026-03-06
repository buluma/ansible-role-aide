# [Ansible role aide](#ansible-role-aide)

Install and configure aide on your system.

|GitHub|GitLab|Downloads|Version|
|------|------|---------|-------|
|[![github](https://github.com/buluma/ansible-role-aide/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-aide/actions)|[![gitlab](https://gitlab.com/shadowwalker/ansible-role-aide/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-aide)|[![downloads](https://img.shields.io/ansible/role/d/buluma/aide)](https://galaxy.ansible.com/buluma/aide)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-aide.svg)](https://github.com/buluma/ansible-role-aide/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-aide/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
  - role: buluma.aide
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-aide/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
  - role: buluma.bootstrap
  - role: buluma.cron
  - role: buluma.postfix
    postfix_myhostname: "smtp.example.com"
    postfix_mydomain: "example.com"
    postfix_myorigin: "example.com"
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.


## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-aide/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.cron](https://galaxy.ansible.com/buluma/cron)|[![Build Status GitHub](https://github.com/buluma/ansible-role-cron/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-cron/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-cron/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-cron)|
|[buluma.postfix](https://galaxy.ansible.com/buluma/postfix)|[![Build Status GitHub](https://github.com/buluma/ansible-role-postfix/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-postfix/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-postfix/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-postfix)|

## [Context](#context)

This role is part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-aide/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|all|
|[Debian](https://hub.docker.com/r/buluma/debian)|all|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|all|

The minimum version of Ansible required is 2.12, tests have been done on:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them on [GitHub](https://github.com/buluma/ansible-role-aide/issues).

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-aide/blob/master/LICENSE).

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)

