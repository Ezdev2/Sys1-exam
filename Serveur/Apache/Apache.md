## 1. Description
Apache est un logiciel de serveur web gratuit et open-source qui alimente environ 46% des sites web à travers le monde. Le nom officiel est Serveur Apache HTTP et il est maintenu et développé par Apache Software Foundation.

Il permet aux propriétaires de sites web de servir du contenu sur le web – d’où le nom « serveur web ».

## 2. Installation
```sudo apt update``` <br>
```sudo apt install apache2``` <br>

## 3. Utilisation
Avant de tester apache2 il faut modifier le paramètre du pare-feu afin de lui donner accès externe aux ports web par défaut.

Répertoriez les profils d’application + ufw + en tapant:
Les profils Apache commencent par WWW:

* WWW *: Ce profil n’ouvre que le port 80 (trafic Web normal, non chiffré)

* Cache WWW *: Ce profil ouvre uniquement le port 8080 (parfois utilisé pour la mise en cache et les proxies Web)

* WWW Full *: ce profil ouvre le port 80 (trafic Web normal non crypté) et le port 443 (trafic crypté TLS / SSL)

* WWW Secure *: Ce profil n’ouvre que le port 443 (trafic crypté TLS / SSL)

Autoriser le trafic sur le port 80
```sudo ufw allow 'WWW'``` <br>

## 4. Vérification de serveur web
```sudo systemctl status apache2``` <br>

## 5. Test
```hostname -I``` <br>

http://adresse Ip (cela affiche la page web de debian)
(pour avoir l'avoir Ip public: 
```sudo apt install curl``` <br>
```curl -4 icanhazip.com``` <br>

## 6. Gestion de processus Apache
- Arreter le serveur web
```sudo systemctl stop apache2``` <br>

- démarrer le serveur Web
```sudo systemctl start apache2``` <br>

- arrêter puis redémarrer le service
```sudo systemctl restart apache2``` <br>

## 7. Hôtes virtuels
Créer le répertoire parent pour le domaine
```sudo mkdir -p /var/www/``` <br>

Attribuer la propriété du repertoire 
```sudo chown -R $USER:$USER /var/www/``` <br>

Permissions
```sudo chmod -R 755 /var/www/``` <br>

Premier test : créer une page html
```nano /var/www//index.html```<br>

Créer un nouveau fichier de configuration pour diffuser le contenu qu'on vient de créer 
```sudo nano /etc/apache2/sites-available/.conf```<br>

Ajouter la configuration:
`<VirtualHost *:80>
   ServerAdmin
   ServerName
   ServerAlias
   DocumentRoot /var/www/
   ErrorLog ${APACHE_LOG_DIR}/error.log
   CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>`

Donne action au fichier .conf qu'on vient de créer 
```sudo a2ensite .conf```<br>

Desactiver la configuration par défaut
```sudo a2dissite 000-default.conf```<br>

Tester l'erreur
```sudo apache2ctl configtest```<br>

redemarrer Apache
```sudo systemctl restart apache2``` <br>

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