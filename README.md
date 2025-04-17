Zsh Config
Ce dépôt contient une configuration Zsh personnalisée, avec des plugins et un thème pour Oh My Zsh.

Sommaire
Installation

Précision importante

Personnalisation

Plugins inclus

Licence

Installation
Cloner le dépôt dans le répertoire des plugins d'Oh My Zsh :

bash
Copier
Modifier
bash <(curl -fsSL https://raw.githubusercontent.com/TeraTech26/zsh-config/main/install_zsh_config.sh)
Recharger la configuration Zsh :

Après l'installation, recharger ta configuration Zsh en exécutant :

bash
Copier
Modifier
source ~/.zshrc
Précision importante
Si aucun des "Aliases" ne fonctionnent, il faut créer le fichier .zsh_aliases dans le répertoire /etc/zsh et copier le code suivant dans le fichier créé :

.zsh_aliases
Copier
Modifier
## Aliases pour la navigation dans les répertoires

alias ..="cd .."
alias ...="cd ../.."
alias home="cd ~"
alias proj="cd /path/to/project"

## Aliases pour la gestion des paquets et des mises à jour (Fedora)

alias update="sudo dnf update -y && sudo dnf upgrade -y"
alias upgrade="sudo dnf upgrade --refresh -y && sudo dnf autoremove -y"
alias install="sudo dnf install -y"
alias remove="sudo dnf remove -y"
alias search="dnf search"
alias clean="sudo dnf clean all"
alias maj="sudo dnf update -y && sudo dnf upgrade -y"

## Aliases pour la gestion des fichiers

alias ll="ls -alF"
alias la="ls -A"
alias l="ls -CF"
alias ls="ls -h"
alias findf="find . -name"
alias editbashrc="nano ~/.bashrc"
alias editzshrc="nano ~/.zshrc"

## Aliases pour la gestion de l'historique

alias history="history | tail -n 20"
alias histgrep="history | grep"

## Aliases pour Git

alias gs="git status"
alias ga="git add ."
alias gc="git commit -m"
alias gp="git push"
alias gl="git log --oneline --graph --decorate --all"

## Aliases pour des commandes courantes

alias mem="free -h"
alias disk="df -h"
alias top="htop"
alias ports="ss -tulnp"
alias sysinfo="uname -a"
alias cpu="lscpu"

## Aliases pour les fichiers compressés

alias untargz="tar -xzvf"
alias unzip="unzip -v"
alias tarball="tar -czvf"
alias zipfile="zip -r"

## Raccourcis utiles

alias grep="grep --color=auto"
alias catn="cat -n"
alias now="date '+%Y-%m-%d %H:%M:%S'"
alias !!="!!"

## Date et heure

alias date="date '+On est le %d/%m/%Y. Et il est %H h %M m %S s.'"
alias datec='date "+%A %d %B %Y"'
alias datef='date "+%Y-%m-%d_%H-%M-%S"'
alias datet="date '+%T'"

## Autres

alias edit="nano"
alias gsave="git add . && git commit -m 'Auto save' && git push"
alias killchrome="pkill chrome"
alias killfirefox="pkill firefox"
Personnalisation
Tu peux personnaliser le fichier ~/.zshrc pour changer le thème ou ajouter d'autres plugins.

Les plugins sont configurés dans le fichier ~/.zshrc sous la section plugins=().

Plugins inclus
git — Commandes Git pratiques.

z — Navigation rapide par historique.

sudo — Simplifie les commandes avec sudo.

autojump — Navigation rapide entre dossiers.

zsh-autosuggestions — Suggestions de commandes en direct.

zsh-syntax-highlighting — Mise en couleur de la syntaxe.

fzf-tab — Auto-complétion avancée avec fzf.

zsh-vi-mode — Mode d’édition façon vi.

zsh-completions — Complétions supplémentaires pour Zsh.

Licence
Ce projet est sous licence [MIT License].
