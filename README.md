# Ansible role for installing Python #

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

An Ansible role for installing [Python](https://www.python.org/).

## Requirements ##

This role uses the `package` Ansible module, so [its
requirements](https://docs.ansible.com/ansible/latest/modules/package_module.html#requirements)
apply.

## Role Variables ##

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| python_install_development_dependencies | A Boolean indicating whether or not to install development dependencies, such as the Python headers.  These dependencies are sometimes required, e.g., when one is required to build a wheel for a Python package. | `false` | No |
| python_install_python2 | A Boolean indicating whether or not to install Python 2 alongside Python 3.  Where possible, we also install the necessary dependencies to use Python 2 as Ansible's discovered Python; unfortunately, this is only possible on Debian Buster.  Note also that no matter the value of this variable, Python 2 will not be installed on Debian Bookworm or later; this is because the corresponding system packages are unavailable for that platform. | `false` | No |

## Dependencies ##

None.

## Installation ##

This role can be installed via the command:

```console
ansible-galaxy install --role-file path/to/requirements.yml
```

where `requirements.yml` looks like:

```yaml
---
- name: python
  src: hhttps://github.com/nholuongut/ansible-role-for-installing-python
```

and may contain other roles as well.

For more information about installing Ansible roles via a YAML file,
please see [the `ansible-galaxy`
documentation](https://docs.ansible.com/ansible/latest/galaxy/user_guide.html#installing-multiple-roles-from-a-file).

## Example Playbook ##

Here's how to use it in a playbook:

```yaml
- hosts: all
  become: true
  become_method: sudo
  tasks:
    - name: Install python
      ansible.builtin.include_role:
        name: python
```

## Contributing ##

We welcome contributions!  Please see [`CONTRIBUTING.md`](CONTRIBUTING.md) for
details.

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
