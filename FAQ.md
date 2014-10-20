FAQ
=====

####à quoi sert GIT?
Git est un logiciel de gestion de versions portable. Il permet de developper des fichiers à plusieurs en parallèle et de fusionner les différentes modifications.

####Où le télécharger ?
Sur http://github.com

####Qu'est-ce qu'un commit ?
Après avoir modifié un fichier, faire un *commit* permet d'enregistrer cette modification, de lui donner un titre et une date. En clair, cela met à jour la version du fichier.

####Qu'est-ce qu'une branche ?
Une *branche* est un espace dans lequel le travail effectué ne modifiera pas le fichier dans les autres branches. Une branche permet de développer son travail dans un conteneur propre et isolé. Les branches peuvent être fusionnées pour mettre en commun les modifications faites aux fichiers.

####Qu'est qu'un fork sur Github ?
Un *fork* est une copie d'un dépôt d'un autre utilisateur. Il permet de travailler dans son propre espace sur un projet développé par ailleurs et de proposer des modifications en *pushant* vers le projet originel. Un *push* doit être accepté par le propriétaire du projet originel.

####un clone ?
Un *clone* est une copie locale d'un dépôt distant. Il permet de travailer hors-ligne et de renvoyer ses modifications plus tard vers le projet en ligne.

####un merge ?
Le *merge* est l'action de fusionner deux branches d'un projet. Si aucun conflit n'apparaît, les branches peuvent être fusionnées automatiquement.  Sinon, il faut résoudre à la main les conflits.

####un diff ?
Le *diff* permet de visualiser les différences des différentes versions des fichiers d'un dépôt. 

##Comment utiliser le logiciel kdiff3 sur mac ?
Téléchargez le à l’adresse suivante : http://sourceforge.net/projects/kdiff3/files/kdiff3/0.9.98/kdiff3-0.9.98-MacOSX-64Bit.dmg/download
Puis déplacez le dans votre dossier « Applications »
Puis configurer votre git en modifiant le fichier texte ~/.gitconfig
Dedans ajouter le code 

```
[difftool "kdiff3"]
    path = /Applications/kdiff3.app/Contents/MacOS/kdiff3
    trustExitCode = false
[difftool]
    prompt = false
[diff]
    tool = kdiff3
[mergetool "kdiff3"]
    path = /Applications/kdiff3.app/Contents/MacOS/kdiff3
    trustExitCode = false
[mergetool]
    keepBackup = false
[merge]
    tool = kdiff3
```

Voilà vous avez en faisant ```git mergetool``` un outil puissant de visualiseur de version.
