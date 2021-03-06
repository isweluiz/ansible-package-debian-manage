[![Ansible Role](https://img.shields.io/ansible/quality/27842.svg)](https://galaxy.ansible.com/isweluiz/ansible_package_debian_manage)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://github.com/isweluiz/ansible-package-debian-manage/blob/master/LICENSE)

ansible_package_debian_manage
=========
Ansible role for managing **Debian** system packages: 

- install
- update
- update security
- clean
- remove

Requirements
------------
Only tested with ansible 2.9.6 min version


Role Variables
--------------
Available variables are listed below, along with default values  `vars/main.yml`  and `defaults/main.yml`

Other way is define those variable in your group hosts or host vars. 

```YAML
# Install 
# List the packages that should be installed here, one per line. Be sure to remove the '[]'
base_system_packages_install: 
  - doscan
  - ncat
  - nmap

# Remove 
# List the packages that should be removed here, one per line. Be sure to remove the '[]'
base_system_packages_remove: 
  - build-essential
  - gcc-4.8
  - make

# Update 
# List the packages that should be update here, one per line. Be sure to remove the '[]'
base_system_packages_update: []
```


Dependencies
------------
No dependencies 


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
      - { role: isweluiz.ansible-package-manage }
```

Remember to use tags based on your needs, otherwise we have the tag `never` with this the task will not run. 
- install
- update
- security
- clean
- remove


#### Install 
```bash
ansible-playbook playbooks/ansible-package.yml -i hosts  -l local -t install
```

#### Update 
```bash
ansible-playbook playbooks/ansible-package.yml -i hosts  -l local -t update
```

#### Security 
```bash
ansible-playbook playbooks/ansible-package.yml -i hosts  -l local -t security
```

#### Clean 
```bash
ansible-playbook playbooks/ansible-package.yml -i hosts  -l local -t clean
```

#### Remove 
```bash
ansible-playbook playbooks/ansible-package.yml -i hosts  -l local -t remove
```


License
-------

MIT

Author Information
------------------
- [Ansible Galaxy](https://galaxy.ansible.com/isweluiz)
- [Github](https://github.com/isweluiz)
- [Linkedin](https://www.linkedin.com/in/isweluiz)
