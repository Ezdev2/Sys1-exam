## 1. Description
Apache est un logiciel de serveur web gratuit et open-source qui alimente environ 46% des sites web à travers le monde. Le nom officiel est Serveur Apache HTTP et il est maintenu et développé par Apache Software Foundation.

Il permet aux propriétaires de sites web de servir du contenu sur le web – d’où le nom « serveur web ».

## 2. Installation
sudo apt update
sudo apt install apache2

## 3. Utilisation
Avant de tester apache2 il faut modifier le paramètre du pare-feu afin de lui donner accès externe aux ports web par défaut.

Répertoriez les profils d’application + ufw + en tapant:
Les profils Apache commencent par WWW:

* WWW *: Ce profil n’ouvre que le port 80 (trafic Web normal, non chiffré)

* Cache WWW *: Ce profil ouvre uniquement le port 8080 (parfois utilisé pour la mise en cache et les proxies Web)

* WWW Full *: ce profil ouvre le port 80 (trafic Web normal non crypté) et le port 443 (trafic crypté TLS / SSL)

* WWW Secure *: Ce profil n’ouvre que le port 443 (trafic crypté TLS / SSL)

Autoriser le trafic sur le port 80
sudo ufw allow 'WWW'

## 4. Vérification de serveur web
sudo systemctl status apache2

## 5. Test
hostname -I

http://adresse Ip (cela affiche la page web de debian)
(pour avoir l'avoir Ip public: 
- sudo apt install curl
- curl -4 icanhazip.com

## 6. Gestion de processus Apache
- Arreter le serveur web
sudo systemctl stop apache2

- démarrer le serveur Web
sudo systemctl start apache2

- arrêter puis redémarrer le service
sudo systemctl restart apache2

## 7. Hôtes virtuels
Créer le répertoire parent pour le domaine
sudo mkdir -p /var/www/

Attribuer la propriété du repertoire 
sudo chown -R $USER:$USER /var/www/

Permissions
sudo chmod -R 755 /var/www/

Premier test : créer une page html
nano /var/www//index.html

Créer un nouveau fichier de configuration pour diffuser le contenu qu'on vient de créer 
sudo nano /etc/apache2/sites-available/.conf

Ajouter la configuration:
<VirtualHost *:80>
   ServerAdmin
   ServerName
   ServerAlias
   DocumentRoot /var/www/
   ErrorLog ${APACHE_LOG_DIR}/error.log
   CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

Donne action au fichier .conf qu'on vient de créer 
sudo a2ensite .conf

Desactiver la configuration par défaut
sudo a2dissite 000-default.conf

Tester l'erreur
sudo apache2ctl configtest

redemarrer Apache
sudo systemctl restart apache2
