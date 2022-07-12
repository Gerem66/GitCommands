# Git

## Configuration de Git
* Pour afficher les couleurs
    - `git config --global color.diff auto`
    - `git config --global color.status auto`
    - `git config --global color.branch auto`
    - `git config --global core.autocrlf true` (Pour ignorer les fins de ligne)
* Se logger
    - `git config --global user.name ___`
    - `git config --global user.email ___`
* Pour les alias
    - `nano ~/.gitconfig`
    - Ajouter les lignes suivantes
        [alias]
        ci = commit
        co = checkout
        st = status
        br = branch

## Commandes

### Projet

| Commande | Détails |
|-|-|
| `git init` | Créer un projet |
| `git clone ...` | Cloner un git, avec `--bare` pour ne télécharger QUE le répertoire de configuration ".git" |
| `git pull` | Permet de télécharger toutes les modifications effectuées |
| `git push` | Permet d'uploader ses commits, il faut être le dernier à push, si d'autres modifications ont été faites entre temps, il faudra pull les nouveaux commits avant de push les miens |

### Ajouts
| Commande | Détails |
|-|-|
| `git status` | Voir le statut des modifications de fichiers |
| `git diff` | Voir les modifications précises apportées |
| `git add fichier1 fichier2 ...` | Ajouter des fichiers ou des répertoires pour les futurs commit |
| `git add .` | Ajouter TOUS les fichiers du projets (sauf .gitignore) /!\ à éviter sur les gros projets |
| `git commit -m "message" ` | Enregistrer les modifications |
| `git commit -a` | Enregstrer tous les fichiers modifiés, visibles en utilisant "git status", équivalent à `git add .` et `git commit` |

### Modifications
| Commande | Détails |
|-|-|
| `git reset --hard master~X` | Permet de charger le Xe dernier commit (master~1 va charger la branche master en ignorant le dernier commit) Permet également d'annuler des commits non pushés |
| `git revert master` | Permet de faire l'inverse du dernier commit (puis push pour l'annuler) |
| `git commit --amend` | Permet de modifier le message du dernier commit effectué |

### Affichage
| Commande | Détails |
|-|-|
| `git log` ou `git show` | Voir les logs du projet |
| `git log -p COMMIT` | Voir les logs des modifications précises apportées |
| `git log --name-only COMMIT` | N'afficher que les noms des fichiers modifiés |
| `git log --stat` | Voir les logs du résumé des commits |

### Branches
| Commande | Détails |
|-|-|
| `git branch` | Permet de voir toutes les branches du projet, et la branche active |
| `git branch ___` | Permet d'ajouter une branche |
| `git checkout ___` | Permet de changer de branche (il ne doit plus y avoir de modifications non commités) |
| `git merge ___` | Permet de fusionner une branche à celle active |
| `git branch -d ___` | Permet de supprimer une branche (si celle-ci a été fisionnée avec une autre, elle devient donc inutile) |
| `git branch -D ___` | Permet de supprimer définitivement une branche et son contenu, même si elle n'a pas été fusionnée (si la branche est une mauvaise idée) |

### Autre
| Commande | Détails |
|-|-|
| `git stash` | Permet de mettre de côté les modifications non commités de manière à pouvoir travailler sur d'autres branches sans avoir à commiter tout de suite |
| `git stash apply` | Restaure les modifications précédemment mises de côté (dans la même branche) |
| `git branch -r` | Permet de lister toutes les branches que le serveur connaît |
| `git grep "TODO"` | Permet de faire une recherche d'un mot clé |
| `git grep -n "TODO"` | Permet également d'afficher les lignes dans lesquels il est présent |

## Source
* https://openclassrooms.com/fr/courses/1233741-gerez-vos-codes-source-avec-git
