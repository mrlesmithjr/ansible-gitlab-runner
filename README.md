# ansible-gitlab-runner

Ansible role to install/configure GitLab runner

## Build Status

### GitHub Actions

![Molecule Test](https://github.com/mrlesmithjr/ansible-gitlab-runner/workflows/Molecule%20Test/badge.svg)

### Travis CI

[![Build Status](https://travis-ci.org/mrlesmithjr/ansible-gitlab-runner.svg?branch=master)](https://travis-ci.org/mrlesmithjr/ansible-gitlab-runner)

## Requirements

For any required Ansible roles, review:
[requirements.yml](requirements.yml)
Replace GitLab token in `defaults/main.yml`

```yaml
gitlab_runner_config:
  url: https://gitlab.com/ci
  # runner token needs to be replaced
  token: TOKEN
  executor: shell
  configure: false
```

## Role Variables

[defaults/main.yml](defaults/main.yml)

## Dependencies

## Example Playbook

[playbook.yml](playbook.yml)

## License

MIT

## Author Information

Larry Smith Jr.

- [@mrlesmithjr](https://twitter.com/mrlesmithjr)
- [mrlesmithjr@gmail.com](mailto:mrlesmithjr@gmail.com)
- [http://everythingshouldbevirtual.com](http://everythingshouldbevirtual.com)

> NOTE: Repo has been created/updated using [https://github.com/mrlesmithjr/cookiecutter-ansible-role](https://github.com/mrlesmithjr/cookiecutter-ansible-role) as a template.
