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

Il suffit d'exécuter la commande `tpenv` dans un terminal, au début de
chaque TP sous Linux.

La liste des fichiers ou dossiers de configuration devant être ainsi
sauvegardés est stockée dans 3 fichiers :

- `~/Documents/Linux/_tpenv/std_includes.txt` ([liste standard](./std_includes.txt))
- `~/Documents/Linux/_tpenv/custom_includes.txt`
- `~/Documents/Linux/_tpenv/custom_excludes.txt`

La commande `tpenv --upgrade` permet de mettre à jour le script et
la liste standard.
Si besoin, vous pouvez modifier les 2 derniers fichiers (initialement
vides) pour spécifier une liste personnalisée de fichiers ou dossiers
à inclure ou exclure.
Les noms de dossier doivent se terminer par `/`. Les caractères `?` et
`*` ne sont pas autorisés, de même que le caractère `/` à une autre
position qu'en fin de ligne.

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
