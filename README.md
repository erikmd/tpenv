# tpenv

## Installation

Exécuter dans un terminal :

```
mkdir -p ~/Documents/Linux/bin && cd ~/Documents/Linux/bin
curl -OL https://github.com/erikmd/tpenv/raw/master/tpenv && chmod a+x tpenv
./tpenv
```

## Syntaxe

```
tpenv
tpenv -v
tpenv --upgrade
tpenv --version
tpenv --help
```

## Résumé

`tpenv` est un script permettant de sauvegarder l'environnement local
de TP (dossiers ou fichiers à la racine du répertoire `~/`) en créant
des liens symboliques vers le dossier `~/Documents/Linux`,
celui-ci étant synchronisé.

Il suffit d'exécuter la commande `tpenv` dans un terminal, une fois
durant le TP sous Linux (au moins à la fin de la première séance, puis
au début de chaque nouvelle séance).

La liste des fichiers ou dossiers devant être ainsi sauvegardés est
stockée dans 3 fichiers :

- `~/Documents/Linux/_tpenv/std_includes.txt` (liste standard)
- `~/Documents/Linux/_tpenv/custom_includes.txt`
- `~/Documents/Linux/_tpenv/custom_excludes.txt`

La commande `tpenv --upgrade` permet de mettre à jour le script et
la liste standard.
Si besoin, vous pouvez modifier les 2 derniers fichiers (initialement vides)
pour spécifier une liste personnalisée de chemins à inclure ou exclure.

Pour plus de facilité, placez le script tpenv dans le dossier
`~/Documents/Linux/bin` (qui est synchronisé).

## Note aux enseignants

Si un fichier ou sous-dossier important de `~/` n'est pas pris en
compte par la version actuelle du script, vous pouvez l'ajouter
directement au fichier `~/Documents/Linux/_tpenv/custom_includes.txt`
ou bien demander son ajout en ouvrant une
[issue](https://github.com/erikmd/tpenv/issues) sur ce dépôt GitHub.

Si vous identifiez un bug, créez une
[issue](https://github.com/erikmd/tpenv/issues) ou envoyez-moi un
[e-mail](https://github.com/erikmd).

## Auteur et licence

Outil conçu par [Érik Martin-Dorel](https://github.com/erikmd),
`tpenv` est un logiciel libre distribué sous licence
[BSD-3](https://opensource.org/licenses/BSD-3-Clause).
