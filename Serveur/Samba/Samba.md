## 1. Description
Samba est un ensemble d'outils permettant de partager des ressources telles que des imprimantes et des fichiers sur un réseau hétérogène. (C’est un serveur fichier)
Un serveur fichier : Un serveur de fichiers permet de partager des données à travers un réseau.

## 2. Fonctions
- Partager un disque Linux pour des machines Windows
- Partager une imprimante Linux avec des machines Windows
- Partager une imprimante Windows à partir d’un hôte LinuxGérer des listes de machines présentes sur le réseau et leur mise à disposition pour tous types de clients (cf : voisinage réseau)

## 3. Installation
sudo apt-get install samba 
apt install samba

## 4. Configuration et paramètrage du serveur
Le fichier /etc/samba/smb.conf permet de configurer Samba. Ce fichier est composé de sections dont le nom est entre crochets) :
[global] : contient les paramètres généraux et les paramètres par défaut des différents partages, (workgroup, server string, netbios name, security, map to guest, dns proxy)
[le_nom_d'un_partage] pour chaque partage (insérer le path, les autorisations)
Créer le dossier à partager, (mkdir nom_de_dossier)
Donner l’autorisation (chmod 777 nom_de_dossier) 
Redemarrer le service samba (/etc/init.d/samba restart)

Pour y rendre il faut :
Editer le fichier nano  /etc/samba/smb.conf

## 5. Etapes après installation
Configuration des machines clientes
Connexion au domaine
