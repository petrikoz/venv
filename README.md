# VENV

[Ansible](http://ansible.com) role which setup Python virtual environment.

* Install and setup VirtualEnvWrapper.
* Setup venv for specific user.

#### Requirements & Dependencies

- [Stouts.deploy](https://github.com/Stouts/Stouts.deploy)
- [Stouts.python](https://github.com/Stouts/Stouts.python)

#### Variables

The role variables and default values.

```yaml
venv_enable: true                                      # Enable the role

venv_wrapper: '/usr/local/bin/virtualenvwrapper.sh'
venv_python: python

venv_workon_home: '/var/www/.venvs'
venv_user: '{{ deploy_user }}'
venv_user_config: '~/.bashrc'

venv_project_dir: '{{ deploy_src_dir }}'
venv_name: '{{ deploy_app_name }}'
```

#### Usage

* Clone dependencies.
* Add `venv` to your roles and change variables in your playbook file.

Example:

```yaml
- hosts: all
  sudo: yes
  roles:
    - Stouts.deploy
    - Stouts.python
    - venv
```

#### License

Licensed under the MIT License. See the LICENSE file for details.
