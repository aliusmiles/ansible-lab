# ansible-lab

Examples for Ansible Lab

## Requirements

* [AWS account](https://aws.amazon.com)
* [Ansible](http://docs.ansible.com/ansible/intro_installation.html)

## HowTo

* Create EC2 instance for control machine
* Install Ansible on it
* Clone this repo:

```bash
git clone https://github.com/aliusmiles/ansible-lab.git
cd ansible-lab
```

## Examples

* ad-hoc commands

```bash
ansible -m ping all
ansible -m ping localhost
ansible -m shell -a "whoami" localhost
```

* playbook commands

```bash
ansible-playbook -i inventory playbook.yml
ansible-playbook -i inventory-prod playbook.yml -l db
ansible-playbook -i inventory-test playbook.yml -t apache-install
```
