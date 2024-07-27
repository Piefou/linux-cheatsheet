# docker-cheatsheet

### Disk management

`docker container run [opt] (image:tag) [command] [args]` Lance un container à partir d'une image

* `-it` avec shell interactif. Ctrl+P + Ctrl+Q pour sortir d'un terminal
* `-d` en arrière-plan
* `-p [hote:container]` mappe un port du container sur l'hôte
* `-P` mapping automatique des ports
* `-v [hote:container:ro]` relie un volume du container à l'hôte, ':ro' pour read-only. Ex : -v /var/path:/data/path:ro; -v volume_nomme:/data/path
* `--name` nomme le container
* `--memory` limite l'allocation mémoire. Ex : --memory 256m
* `--cpus` limite l'allocation cpu ; Décimal < 1 : pourcentage du nombre de cpus disponibles ; Entier >= 1 : nombre de cpus. Ex : --cpus 2, --cpus 0.5
* `--rm` supprime le filesystem du container une fois terminé
* `--user` spécifie l'utilisateur à utiliser
* `--restart=[on-failure | always]` redémarrage automatique du container
* `--network [reseau]` indique le réseau par défaut sur lequel se connecter

## Package management

### APT


### DNF

Configurations files :
* /etc/dnf/dnf.conf : Generic DNF configuration
* /etc/yum.repos.d/ : Repositories configuration

`dnf check-update` Check for updates on installed packages

`dnf upgrade` Update all the installed packages

`dnf search <keyword>` Search for packages with keyword in its name

`dnf install <package-name>` Install this package

`dnf install <https://<url-to-the-repo.com/repo.rpm>` Install this repository to get access to its packages

`dnf remove <package-name>` Install this package

