## Setup of Ansible Sandbox Lab

If you have provisioned the jumphost for the first time, we need to run through some pre-requisites.

```sh
subscription-manager register --activationkey={{activation_key}} --org={{org_id}}
subscription-manager repos --enable=rhel-7-server-ansible-2.9-source-rpms
yum install python3 python3-pip
pip3 install ansible
```
