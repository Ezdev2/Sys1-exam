[Go to Readme.md](https://github.com/Ezdev2/Sys1-exam/blob/339c2029e1b0f42828993adb922f40f8ca4defb9/README.md)

***

## 1. Description
Nginx (Engine X, prononcez [n-gèn-x]) est un serveur Web asynchrone écrit par Igor Sysoev pour les
besoins d'un site russe à très fort trafic. Il peut être configuré pour faire office de serveur reverse proxy
Web et de serveur proxy de messagerie électronique (IMAP/POP3).

## 2. Installation
Sur linux
Mettre à jour la liste des paquets
```$ sudo apt install update``` <br>

Installer le paquet nginx
```$ sudo apt install nginx``` <br>

Sur windows
aller sur le lien de téléchargement officiel de
Nginx a l’adress suivant :
[Nginx](https://www.nginx.org/en/download.html/)
et télécharger la version pour windows qui
vous convienne

## 3. Configuration
Les fichiers de configuration de nginx se trouves dans le dossier /etc/nginx
les fichiers qui nous intéresse sont :
- ```nginx.conf``` : Le fichier de configuration globale du serveur.
- ```mime.types``` : La liste des types MIME résolus par les extensions de fichiers
- ```sites-available``` : Contient les fichiers de configurations de vos sites ou services (un fichier par
préoccupation/site/service).
- ```sites-enabled``` : Doit contenir des liens symboliques vers les fichiers de site-available que vous
souhaitez activer.
- ```conf.d``` : Emplacement pour appliquer les paramètres communs à tous les sites.

Le ```nginx.conf``` par défaut
Le fichier ```nginx.conf``` est l'élément névralgique de votre serveur Nginx. Nous allons voir à quoi
ressemble un fichier ```nginx.conf``` par défaut sous Linuxmint

Listes des commandes à savoir

Vérifier la syntaxe de la configuration
```$ sudo nginx -t``` <br>

Démarrer le service Nginx
```$ sudo systemctl start nginx``` <br>

On peut aussi redémarrer le service Nginx s’il est déjà actif
```$ sudo systemctl restart nginx``` <br>

Arrêter le service Nginx
```$ sudo systemctl stop nginx``` <br>

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