FAQ
=====

####à quoi sert GIT?
Git est un logiciel de gestion de versions portable. Il permet de developper des fichiers à plusieurs en parallèle et de fusionner les différentes modifications.

####Où le télécharger ?
Sur http://github.com

####Qu'est-ce qu'un commit ?
Après avoir modifié un fichier, faire un *commit* permet d'enregistrer cette modification, de lui donner un titre et une date. En clair, cela met à jour la version du fichier.

####Qu'est-ce qu'une branche ?
Une *branche* est un espace dans lequel le travail effectué ne modifiera pas le fichier dans les autres branches. Il permet de créer sa propre version du fichier. Les branches peuvent être fusionnées pour mettre en commun les modifications faites aux fichiers.

####Qu'est qu'un fork ?
Un *fork* est une branche faite à partir du projet d'un autre utilisateur. Le *fork* permet de ttravailler dans son propre espace avant de proposer ses modifications en *pushant* vers le projet originel pour fusionner les modifications. Un *push* doit être accepté par l'ayanyt-droit du projet.

####un clone ?
Un *clone* est une copie locale d'un projet. Il permet de travailer hors-ligne et de renvoyer ses modifications plus tard vers le prjet en ligne.

####un merge ?
Le *merge* est l'inverse de la *branche* C'est la fusion d'une branche dans l'autre, les versions étant fusionnées automatiquement si possible. 

####un diff ?
Si la fusion automatique n'est pas possible, l'utilisateur doit choisir manuellement les options de fusion. Le *diff* permet l'affichage des différentes versions et le choix des elements de chaque version.

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
