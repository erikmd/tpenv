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
tpenv [-v]
tpenv --upgrade
tpenv --help
```

## Résumé

`tpenv` est un script permettant de sauvegarder l'environnement local
de TP (dossiers ou fichiers à la racine du répertoire ~/) en créant
des liens symboliques vers le dossier `~/Documents/Linux`,
celui-ci étant synchronisé.

Il suffit d'exécuter la commande `tpenv` dans un terminal, une fois
durant le TP sous Linux (à la fin de la première séance, puis au début
de chaque nouvelle séance).

La liste des fichiers ou dossiers devant être ainsi sauvegardés est
stockées dans 3 fichiers :

- `~/Documents/Linux/_tpenv/std_includes.txt` (liste standard)
- `~/Documents/Linux/_tpenv/custom_includes.txt`
- `~/Documents/Linux/_tpenv/custom_excludes.txt`

La commande `tpenv --upgrade` permet de mettre à jour la liste standard.

Si besoin, vous pouvez modifier les 2 derniers fichiers (initialement vides)
pour spécifier une liste personnalisée de chemins à inclure ou exclure.
