+++
date = '2025-01-13T13:08:53+01:00'
draft = false
title = 'Commandes Linux'
+++
### Commandes utiles sous Linux<!--more-->

## Afficher un fichier de sans les commentaires.

```bash
grep -v '^\s*#' fichier.txt | grep -v '^$'
```
# Description
Cette commande est utilisée pour filtrer un fichier texte (`fichier.txt`) en supprimant toutes les lignes vides et les lignes de commentaires.

{{< details "Explications" >}}
1. **`grep -v '^\s*#' fichier.txt`** :
   - `grep` est un utilitaire de recherche de texte.
   - L'option `-v` inverse la recherche (affiche tout sauf ce qui correspond au modèle).
   - Le modèle `'^\s*#'` correspond aux lignes qui commencent par un ou plusieurs espaces (`\s*`), suivis d'un `#` (commentaires en ligne dans de nombreux fichiers de configuration).
   - Cette première commande supprime donc toutes les lignes qui commencent par un commentaire (`#`).

2. **`grep -v '^$'`** :
   - Cette partie filtre les lignes vides du fichier.
   - `^$` correspond aux lignes vides (aucun caractère entre le début `^` et la fin de la ligne `$`).
   - En utilisant `-v`, toutes les lignes vides sont supprimées.
{{< /details >}}
## Autre commande ....