Ansible roles meta-repository
=========

Used to store other role repositories in one place with name changed to ansible-galaxy name (to be compatible with dependency role names provided in meta files) as git submodules.


BREAKING CHANGES !!!
------------
Please update role names in your playbooks before fetching this repo, review folder names here or in requirements.yml file and do all he changes from your last fetched commit!


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
Or just do ```git pull``` if it did all updates already, but recommended option is above.

Don't forget to copy/move roles to your (or one of the system's default roles folder) or use it as that folder in ansible config file via ```roles_path``` parameter (or by defining it in ```ANSIBLE_ROLES_PATH``` environment variable).

Alternative options is to do ```ansible-galaxy install -r requirements.yml``` to download all galaxy roles into your "roles_path" folder.


Examples
----------------

Examples ( inventories, playbooks etc. ) can be found [here](https://github.com/caermeglaeddyv/examples/tree/dev/ansible).

It's highly recommended to start you test deploys from there, especially if you use Google Cloud Platform or VMware vCenter as your infrastructure, for now that [repository](https://github.com/caermeglaeddyv/examples) contains [Packer](https://github.com/caermeglaeddyv/examples/tree/dev/packer) and [Terraform](https://github.com/caermeglaeddyv/examples/tree/dev/terraform) examples to build templates and deploy machines on this platforms.


License
-------

[Apache 2.0](https://github.com/caermeglaeddyv/ansible-roles/blob/dev/LICENSE)


Author Information
------------------

Copyright 2020 [caermeglaeddyv](https://github.com/caermeglaeddyv)
