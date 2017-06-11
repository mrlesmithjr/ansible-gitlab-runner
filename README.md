# Role Name

An [Ansible] role to install/configure [GitLab] - [runner]

## Requirements

None

## Role Variables

```yaml
---
# defaults file for ansible-gitlab-runner
gitlab_runner_check_interval: 0
gitlab_runner_concurrent_jobs: 1

gitlab_runner_config:
  url: 'https://gitlab.com/ci'
  token: ''
  executor: 'shell'

gitlab_runner_debian_package:
  key: '{{ gitlab_runner_uri }}/gpgkey'
  package: '{{ gitlab_runner_uri }}/packages/{{ ansible_distribution|lower }}/{{ ansible_distribution_release|lower }}/gitlab-ci-multi-runner_{{ gitlab_runner_version }}_amd64.deb'
  repos:
    - 'deb https://packages.gitlab.com/runner/gitlab-ci-multi-runner/{{ ansible_distribution|lower }}/ {{ ansible_distribution_release|lower }} main'
    - 'deb-src https://packages.gitlab.com/runner/gitlab-ci-multi-runner/{{ ansible_distribution|lower }}/ {{ ansible_distribution_release|lower }} main'

gitlab_runner_uri: 'https://packages.gitlab.com/runner/gitlab-ci-multi-runner'

gitlab_runner_version: 9.2.0
```

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: gitlab_runner
  vars:
  roles:
    - role: ansible-gitlab-runner
  tasks:
```

## License

BSD

## Author Information

Larry Smith Jr.

-   [@mrlesmithjr]
-   <http://everythingshouldbevirtual.com>
-   mrlesmithjr [at] gmail.com

[@mrlesmithjr]: https://www.twitter.com/mrlesmithjr

[ansible]: https://www.ansible.com

[gitlab]: https://www.gitlab.com

[runner]: https://docs.gitlab.com/runner/
