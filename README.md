Ansible roles meta-repository
=========

Used to store other role repositories in one place with simplified names (without "ansible-role-" suffix) as git submodules.


Requirements
------------

clone repo with all submodules:
```bash
git clone --recurse-submodules https://github.com/caermeglaeddyv/ansible-roles.git
```
Update all submodules with latest changes
```bash
git submodule update --remote --merge
```
Or just do ```git pull``` if i did all updates already, but recommended option is above.

Don't forget to copy/move roles to your (or one of the system's default roles folder) or use it as that folder in ansible config file via ```roles_path``` parameter (or by defining it in ```ANSIBLE_ROLES_PATH``` environment variable).


Examples
----------------

Examples ( inventories, playbooks etc. ) can be found [here](https://github.com/caermeglaeddyv/examples/tree/dev/ansible).

It's highly recommended to start you test deploys from there, especially if you use Google Cloud Platform or VMware vCenter as your infrastructure, for now that [repository](https://github.com/caermeglaeddyv/examples) contains [Packer](https://github.com/caermeglaeddyv/examples/tree/dev/packer) and [Terraform](https://github.com/caermeglaeddyv/examples/tree/dev/terraform) examples to build templates and deploy machines on this platforms.


License
-------

[Apache 2.0](https://github.com/caermeglaeddyv/ansible-role-rear/blob/dev/LICENSE)


Author Information
------------------

Copyright 2020 [caermeglaeddyv](https://github.com/caermeglaeddyv)
