Add a directory named as your username and place the following files before running the playbook:

```
<username>/
├── gitconfig              → ~/.gitconfig
├── config                 → ~/.ssh/config
├── hosts                  → /etc/hosts
├── settings_gitlab_com.xml → ~/.m2/settings.xml
├── enovea_rsa*            → ~/.ssh/
├── k9s/                   → ~/.config/k9s/
│   ├── config.yaml
│   └── aliases.yaml
├── lazygit/               → ~/.config/lazygit/
│   └── config.yml
├── glab-cli/              → ~/.config/glab-cli/
│   ├── config.yml
│   └── aliases.yml
├── argocd/                → ~/.config/argocd/
│   └── config
├── wezterm/               → ~/.config/wezterm/
│   └── wezterm.lua
├── p10k.zsh               → ~/.p10k.zsh
├── docker/                → ~/.docker/
│   └── config.json
└── claude/                → ~/.claude/
    └── settings.json
```
