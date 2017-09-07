cfme-ocp-manager
=========

This role adds all OpenShift clusters in an inventory, in the 'oc' group, to a CloudForms Management Engine

Requirements
------------

This requires
* CloudForms Management Engine >4.1
* OpenShift Container Platform >3.2

Role Variables
--------------

The following variables are the defaults for a project and are found in defaults/main.yml.
```
---
# defaults file for kevensen.cfme-ocp-manager
cfme_user: admin
cfme_password: smartvm
cfme_api_url: https://localhost
cfme_api_port: 443
```

Dependencies
------------

No dependencies.

Example Playbook
----------------
```yaml
---
# file: cfme-add-ocp-provider.yml
- hosts: cfme
  roles:
  - kevensen.cfme-ocp-manager
```

Example Inventory
-----------------
```ini
[oc]
openshift.example.com

[cfme]
cfme.example.com
```

Example Execution
-----------------
```shell
ansible-playbook -i inventory_file cfme-add-ocp-provider.yml
```

License
-------

GPLv3

Author Information
------------------

Ken Evensen
