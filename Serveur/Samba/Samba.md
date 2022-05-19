[Go to Readme.md](https://github.com/Ezdev2/Sys1-exam/blob/339c2029e1b0f42828993adb922f40f8ca4defb9/README.md)

***

## 1. Description
Samba est un ensemble d'outils permettant de partager des ressources telles que des imprimantes et des fichiers sur un réseau hétérogène. (C’est un serveur fichier)
Un serveur fichier : Un serveur de fichiers permet de partager des données à travers un réseau.

## 2. Fonctions
- Partager un disque Linux pour des machines Windows
- Partager une imprimante Linux avec des machines Windows
- Partager une imprimante Windows à partir d’un hôte LinuxGérer des listes de machines présentes sur le réseau et leur mise à disposition pour tous types de clients (cf : voisinage réseau)

## 3. Installation
```sudo apt-get install samba ``` <br>
```apt install samba```

## 4. Configuration et paramètrage du serveur
Le fichier /etc/samba/smb.conf permet de configurer Samba. Ce fichier est composé de sections dont le nom est entre crochets) :
[global] : contient les paramètres généraux et les paramètres par défaut des différents partages, (workgroup, server string, netbios name, security, map to guest, dns proxy)
[le_nom_d'un_partage] pour chaque partage (insérer le path, les autorisations)
Créer le dossier à partager, ```mkdir nom_de_dossier``` <br>
Donner l’autorisation ```chmod 777 nom_de_dossier``` <br>
Redemarrer le service samba ```/etc/init.d/samba restart``` <br>

Pour y rendre il faut :
Editer le fichier ```nano  /etc/samba/smb.conf``` <br>

## 5. Etapes après installation
Configuration des machines clientes
Connexion au domaine

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