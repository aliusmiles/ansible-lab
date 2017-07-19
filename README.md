# ansible-lab
Examples for Ansible Lab

## Requirements
* On Windows: Linux VM or Virtualbox and Vagrant
* [Ansible](http://docs.ansible.com/ansible/intro_installation.html)
* [AWS account](https://aws.amazon.com)
* [awscli](http://docs.aws.amazon.com/cli/latest/userguide/installing.html)

## HowTo
* On Windows: `vagrant up && vagrant ssh`
* `aws configure`
* `git clone https://github.com/aliusmiles/ansible-lab.git`
* `cd ansible-lab`
* `ansible-playbook aws/provision.yml`
* Removing test instances: `ansible-playbook aws/teardown.yml`

## Notes
* Custom AWS region could be set in file _aws/vars.yml_
* Custom instance or server could be set in _inventory_ file manually, in which case _aws/provision.yml_ is not needed
