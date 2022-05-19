## 1. Description
Nginx (Engine X, prononcez [n-gèn-x]) est un serveur Web asynchrone écrit par Igor Sysoev pour les
besoins d'un site russe à très fort trafic. Il peut être configuré pour faire office de serveur reverse proxy
Web et de serveur proxy de messagerie électronique (IMAP/POP3).

## 2. Installation
Sur linux
Mettre à jour la liste des paquets
$ sudo apt install update

Installer le paquet nginx
$ sudo apt install nginx

Sur windows
aller sur le lien de téléchargement officiel de
Nginx a l’adress suivant :
[Nginx](https://www.nginx.org/en/download.html/)
et télécharger la version pour windows qui
vous convienne

## 3. Configuration
Les fichiers de configuration de nginx se trouves dans le dossier /etc/nginx
les fichiers qui nous intéresse sont :
- nginx.conf : Le fichier de configuration globale du serveur.
- mime.types : La liste des types MIME résolus par les extensions de fichiers
- sites-available : Contient les fichiers de configurations de vos sites ou services (un fichier par
préoccupation/site/service).
- sites-enabled : Doit contenir des liens symboliques vers les fichiers de site-available que vous
souhaitez activer.
- conf.d : Emplacement pour appliquer les paramètres communs à tous les sites.

Le nginx.conf par défaut
Le fichier nginx.conf est l'élément névralgique de votre serveur Nginx. Nous allons voir à quoi
ressemble un fichier nginx.conf par défaut sous Linuxmint

Listes des commandes à savoir

Vérifier la syntaxe de la configuration
$ sudo nginx -t

Démarrer le service Nginx
$ sudo systemctl start nginx

On peut aussi redémarrer le service Nginx s’il est déjà actif
$ sudo systemctl restart nginx

Arrêter le service Nginx
$ sudo systemctl stop nginx