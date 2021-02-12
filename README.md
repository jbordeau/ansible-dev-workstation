# Ansible to install a development workstation

## Getting started

Install the prerequisites
```bash
ansible-galaxy install -r requirements.yml
ansible-galaxy collection install -r requirements.yml
```

Run a playbook on localhost:
```bash
ansible-playbook -i hosts -K docker.yml
```