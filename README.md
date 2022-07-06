# Ansible to install a development workstation

TODO
* kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-using-native-package-management
* k9s: https://github.com/derailed/k9s
* helm: https://helm.sh/docs/intro/install/


## Getting started

Install the prerequisites
```bash
ansible-galaxy install -r requirements.yml
ansible-galaxy collection install -r requirements.yml
```

Run a playbook on localhost:
```bash
ansible-playbook -K main.yml
```
