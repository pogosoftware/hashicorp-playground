# hashicorp-playground

# Requirements
* [pre-commit](https://pre-commit.com/#installation)
* [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

# Multipass
Multipass will create virtual machines on which all Hashicorp products will be installed and running.
To run multipass you need have generated ssh key which ansible will be using to connect to there vm's.

There are 3 variables inside `ansible/vars/multipass` that allows you to setup ssh access.
```yaml
multipass_ansible_user: ansible
multipass_ansible_ssh_private_key_file: "~/.ssh/ansible"
multipass_ssh_public_key: "~/.ssh/ansible.pub"
```

```bash
ansible-playbook 00_multipass_deployment.yml
```
