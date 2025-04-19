# Zsh Config

Ce dépôt contient une configuration Zsh personnalisée, avec des plugins et un thème pour Oh My Zsh.

## Sommaire

- [Installation](#installation)
- [Précision importante](#précision-importante)
- [Personnalisation](#personnalisation)
- [Plugins inclus](#plugins-inclus)
- [Licence](#licence)

## Installation

1. **Cloner le dépôt** dans le répertoire des plugins d'Oh My Zsh :

   ```bash
   bash <(curl -fsSL https://github.com/TeraTech26/zsh-fedora/blob/zsh-fedora/install_zsh_config.sh)
   ```

2. **Recharger la configuration Zsh** :

   Après l'installation, recharger ta configuration Zsh en exécutant :

   ```bash
   source ~/.zshrc
   ```

## Précision importante

Si les alias ne fonctionnent pas, crée le fichier .zsh_aliases dans /etc/zsh avec ce contenu :

\`\`\`bash
# Navigation
alias ..="cd .."
alias ...="cd ../.."
alias home="cd ~"
alias proj="cd /path/to/project"

# Gestion de paquets (Fedora)
alias update="sudo dnf update -y && sudo dnf upgrade -y"
alias upgrade="sudo dnf upgrade --refresh -y && sudo dnf autoremove -y"
alias install="sudo dnf install -y"
alias remove="sudo dnf remove -y"
alias search="dnf search"
alias clean="sudo dnf clean all"
alias maj="sudo dnf update -y && sudo dnf upgrade -y"

# Fichiers
alias ll="ls -alF"
alias la="ls -A"
alias l="ls -CF"
alias ls="ls -h"
alias findf="find . -name"
alias editbashrc="nano ~/.bashrc"
alias editzshrc="nano ~/.zshrc"

# Historique
alias history="history | tail -n 20"
alias histgrep="history | grep"

# Git
alias gs="git status"
alias ga="git add ."
alias gc="git commit -m"
alias gp="git push"
alias gl="git log --oneline --graph --decorate --all"

# Commandes utiles
alias mem="free -h"
alias disk="df -h"
alias top="htop"
alias ports="ss -tulnp"
alias sysinfo="uname -a"
alias cpu="lscpu"

# Fichiers compressés
alias untargz="tar -xzvf"
alias unzip="unzip -v"
alias tarball="tar -czvf"
alias zipfile="zip -r"

# Divers
alias grep="grep --color=auto"
alias catn="cat -n"
alias now="date '+%Y-%m-%d %H:%M:%S'"
alias !!="!!"

# Date/Heure
alias date="date '+On est le %d/%m/%Y. Et il est %H h %M m %S s.'"
alias datec='date "+%A %d %B %Y"'
alias datef='date "+%Y-%m-%d_%H-%M-%S"'
alias datet="date '+%T'"

# Autres
alias edit="nano"
alias gsave="git add . && git commit -m 'Auto save' && git push"
alias killchrome="pkill chrome"
alias killfirefox="pkill firefox"
\`\`\`

Personnalisation
Tu peux modifier ~/.zshrc pour changer le thème ou ajouter des plugins. La ligne plugins=() définit ceux à charger.

Plugins inclus
git — Commandes Git utiles

z — Navigation rapide entre dossiers

sudo — Préfixe automatique sudo

autojump — Historique de navigation intelligent

zsh-autosuggestions — Suggestions de commandes

zsh-syntax-highlighting — Coloration syntaxique

fzf-tab — Auto-complétion améliorée

zsh-vi-mode — Édition type vi

zsh-completions — Complétions supplémentaires

Licence
Sous licence MIT.
