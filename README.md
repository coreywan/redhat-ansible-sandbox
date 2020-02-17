## Setup of Ansible Sandbox Lab

If you have provisioned the jumphost for the first time, we need to run through some pre-requisites.

From root run:

```sh
subscription-manager register --activationkey={{activation_key}} --org={{org_id}}
subscription-manager repos --enable=rhel-7-server-ansible-2.9-source-rpms
yum install git python3 python3-pip
pip3 install ansible
```


From student, run your playbook to setup the environment

```sh
git clone https://github.com/coreywan/redhat-ansible-sandbox.git
cd redhat-ansible-sandbox
ansible-playbook -i inventory pb-config-manage.yml --ask-vault-pass
```