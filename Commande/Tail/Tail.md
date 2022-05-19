## 1. Description
Tail est une commande linux utiliser pour afficher les derniers ligne d’un fichier.
Il affiche habituellement les 10 dernières lignes mais avec des paramètres on peut faire des
commande plus personnaliser.

## 2. Utilisation
Afficher les dix dernières lignes d’un fichier :
```$ tail nom_du_fichier```

Limiter le nombre de lignes affichées avec l’option -n# (# étant un nombre).
```$ tail -n# nom_du_fichier```

Afficher les dernières octets d’un fichier avec l’option -c# (# étant un nombre).
```$ tail -c# nom_du_fichier```

Surveiller les modifications apportées à un fichier avec l'option -f
```$ tail -f nom_du_fichier```

Récupérer les sorties de tail
```$ tail nom_du_fichier | autre_commande```

Comment avoir de l’aide
```$ tail --help```
```$ man tail```