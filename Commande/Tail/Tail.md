[Go to Readme.md](https://github.com/Ezdev2/Sys1-exam/blob/339c2029e1b0f42828993adb922f40f8ca4defb9/README.md)

***

## 1. Description
Tail est une commande linux utiliser pour afficher les derniers ligne d’un fichier.
Il affiche habituellement les 10 dernières lignes mais avec des paramètres on peut faire des
commande plus personnaliser.

## 2. Utilisation
Afficher les dix dernières lignes d’un fichier :
```$ tail nom_du_fichier``` <br>

Limiter le nombre de lignes affichées avec l’option -n# (# étant un nombre).
```$ tail -n# nom_du_fichier``` <br>

Afficher les dernières octets d’un fichier avec l’option -c# (# étant un nombre).
```$ tail -c# nom_du_fichier``` <br>

Surveiller les modifications apportées à un fichier avec l'option -f
```$ tail -f nom_du_fichier``` <br>

Récupérer les sorties de tail
```$ tail nom_du_fichier | autre_commande``` <br>

Comment avoir de l’aide
```$ tail --help``` <br>
```$ man tail``` <br>

***

## Les serveurs:
- [NFS](https://github.com/Ezdev2/Sys1-exam/blob/4750ad7d4892b82a726086d65c02a70691cd419f/Serveur/NFS/NFS.md)
- [Apache](https://github.com/Ezdev2/Sys1-exam/blob/4750ad7d4892b82a726086d65c02a70691cd419f/Serveur/Apache/Apache.md)
- [Nginx](https://github.com/Ezdev2/Sys1-exam/blob/374a9c44fa839a2b5d9c3ce764b1ac481817113a/Serveur/Nginx/Nginx.md)
- [Samba](https://github.com/Ezdev2/Sys1-exam/blob/5e6f69982d0ecc74b55fad6e14ad86d2690bcf5e/Serveur/Samba/Samba.md)
- [VSFTPD](https://github.com/Ezdev2/Sys1-exam/blob/d1ecfe08599c1c13d726cc10440d7fea9b4b008f/Serveur/VSFTPD/VSFTPD.md)

## Les Commandes
- [Nmap](https://github.com/Ezdev2/Sys1-exam/blob/710bf9e865e272ccfebcfa9d0a84604f9a2c784e/Commande/Nmap/Nmap.md)
- [Iptable](https://github.com/Ezdev2/Sys1-exam/blob/710bf9e865e272ccfebcfa9d0a84604f9a2c784e/Commande/Iptable/Iptable.md)
- [Tail](https://github.com/Ezdev2/Sys1-exam/blob/710bf9e865e272ccfebcfa9d0a84604f9a2c784e/Commande/Tail/Tail.md)