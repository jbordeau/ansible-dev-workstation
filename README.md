# Ansible Dev Workstation

Playbook Ansible pour provisionner un poste de dev sous Debian/Ubuntu.

## Ce qui est installé

### Paquets APT (tools.yml)
git, curl, vim, openvpn, jq, vagrant, bat, ripgrep, thefuck, yakuake, snapd, htop, Google Chrome, WezTerm

### Docker (docker.yml)
Docker via le rôle `geerlingguy.docker`

### Shell (zsh.yml)
Zsh + Antigen (mvn, git, debian, zsh-z, jump, common-aliases, thefuck), fonts Powerline, fzf

### Mise (mise.yaml)
Gestionnaire de versions pour les outils CLI :
- **Dev** : java, maven, node, quarkus, go, aws-cli, rust, fzf, lazygit, delta
- **K8s** : kubectl, kubectx, helm, helm-diff, helmfile, k9s, minikube, kind
- **IA** : opencode, ccstatusline, ollama, claude-code
- **Ops** : argocd, httpie-go

### IDE (intellij.yml, vscode.yml)
- IntelliJ IDEA Ultimate
- VS Code + extensions Java et Quarkus

### Apps desktop
- **Communication** (communication.yml) : Teams, Signal, Slack
- **Entertainment** (entertainment.yml) : Spotify

### Config utilisateur (user_config.yml)
Copie des fichiers de config personnels (gitconfig, SSH, Maven, k9s, lazygit, glab-cli, argocd, wezterm, Docker, Claude Code). Voir [users/files/README.md](users/files/README.md) pour la structure attendue.

## Utilisation

### Prérequis

```bash
sudo apt install ansible
ansible-galaxy install -r requirements.yml
ansible-galaxy collection install -r requirements.yml
```

### Lancer le playbook complet

```bash
ansible-playbook -K main.yml
```

### Lancer un playbook spécifique

```bash
ansible-playbook -K tools.yml
```

### Lancer uniquement certains tags

```bash
ansible-playbook -K tools.yml --tags chrome,wezterm
ansible-playbook -K communication.yml --tags slack
```

### Config utilisateur

Avant de lancer `user_config.yml`, placer ses fichiers dans `users/files/<username>/` (voir le README dédié), puis décommenter l'import dans `main.yml` ou lancer directement :

```bash
ansible-playbook -K user_config.yml
```
