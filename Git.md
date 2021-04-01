# Git

## Configuration de Git
* Pour afficher les couleurs
    - git config --global color.diff auto
    - git config --global color.status auto
    - git config --global color.branch auto
* Se logger
    - git config --global user.name ___
    - git config --global user.email ___
* Pour les alias
    - nano ~/.gitconfig
    - Ajouter les lignes suivantes
        [alias]
        ci = commit
        co = checkout
        st = status
        br = branch

## Commandes de projet

* git init                              | Créer un projet
* git clone ...                         | Cloner un git
* Ajouter l'argument --bare             | Ne télécharger QUE le répertoire de configurations ".git"
* git status                            | Voir le statut des modifications de fichiers
* git diff                              | Voir les modifications précises apportées
* git add fichier1 fichier2 ...         | Ajouter des fichiers pour les futurs commit
* git commit                            | Enregistrer les modifications
* git commit -a                         | Enregstrer tous les fichiers modifiés, visibles en utilisant "git status"
* git commit fichier1 fichier2 ...      | Enregistrer des fichiers précis
* git log                               | Voir les logs du projet
* git log -p                            | Voir les logs des modifications précises apportées
* git log --stat                        | Voir les logs du résumé des commits
* git commit --amend                    | Permet de modifier le message du dernier commit effectué
* git pull                              | Permet de télécharger toutes les modifications effectuées
* git push                              | Permet d'uploader ses commits, il faut être le dernier à push,
                                          Si d'autres modifications ont été faites entre temps, il faudra pull les nouveaux commits avant de push les miens
* git branch                            | Permet de voir toutes les branches du projet, et la branche active
* git branch ___                        | Permet d'ajouter une branche
* git checkout ___                      | Permet de changer de branche (il ne doit plus y avoir de modifications non commités)
* git merge ___                         | Permet de fusionner une branche à celle active
* git branch -d ___                     | Permet de supprimer une branche (si celle-ci a été fisionnée avec une autre, elle devient donc inutile)
* git branch -D ___                     | Permet de supprimer définitivement une branche et son contenu, même si elle n'a pas été fusionnée (si la branche est une mauvaise idée)
* git stash                             | Permet de mettre de côté les modifications non commités de manière à pouvoir travailler sur d'autres branches sans avoir à commiter tout de suite
* git stash apply                       | Restaure les modifications précédemment mises de côté (dans la même branche)
* git branch -r                         | Permet de lister toutes les branches que le serveur connaît
* git tag NOMTAG IDCOMMIT               | Ajouter un tag sur un commit
* git push --tags                       | Permet d'envoyer les tags lors d'un push
* git tag -d NOMTAG                     | Permet de supprimer un tag
* git grep "TODO"                       | Permet de faire une recherche d'un mot clé
* git grep -n "TODO"                    | Permet également d'afficher les lignes dans lesquels il est présent
* .gitignore >> fichier1 \n fichier2 ...| Permet d'ignorer des fichiers

## Source
* https://openclassrooms.com/fr/courses/1233741-gerez-vos-codes-source-avec-git