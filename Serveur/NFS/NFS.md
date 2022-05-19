[Go to Readme.md](https://github.com/Ezdev2/Sys1-exam/blob/339c2029e1b0f42828993adb922f40f8ca4defb9/README.md)

***

## 1. Description
Le NFS, pour Network File System, est un protocole permettant à un ordinateur d'accéder à des fichiers extérieurs via un réseau. Développé dans les années 80, le NFS s'est ensuite imposé comme la norme en matière de serveur de fichiers.

## 2. Versions
Les premières versions, que ce soit NFS v1, NFS v2 ou NFS v3 n'étaient pas sécurisées : à l'époque, la sécurité n'était pas une priorité. Il y avait également des limitations sur la taille des paquets (8 Ko) et la taille maximale d'un fichier transférable (2 Go) avant l'arrivée de NFS v3.

C'est en 2000, avec la sortie de NFSv4 que le protocole a fortement évolué pour intégrer des fonctionnalités liées à la sécurité. Il a tellement évolué, que le NFSv4 marque une véritable rupture vis-à-vis des versions précédentes (et cela n'est pas sans conséquence, nous en reparlerons). Depuis, le protocole NFS a eu le droit à plusieurs mises à jour, en version 4.1 en 2010 et un peu plus récemment, en 2016, en version 4.2.
Le protocole NFS v4 prend en charge complètement la sécurité avec l'authentification via Kerberos et il s'appuie sur des connexions TCP avec suivi de l'état (stateful).

## 3. Créer un paratge NFS sous Debian
Après cette introduction théorique, nous allons passer à la pratique. Pour cela, nous allons utiliser deux machines sous Linux (Debian 11), mais vous pouvez utiliser d'autres distributions.

- Un serveur Debian qui jouera le rôle de serveur NFS, avec un partage : /home/nfs
- Adresse IP : 192.168.0.250/24
- Un poste client Debian qui jouera le rôle de client NFS
- Adresse IP : 192.168.10.10/24

## 4. Installation

Coté serveur: 
```apt-get nfs-kernel-server``` <br>
```apt install nfs-kernel-server(se référer sur les vidéo semaine 5 sur l’installation des packages)``` <br>

Créer le dossier et/ou fichierà paartager dans:
```/etc/exports``` <br>

Créer un repertoire
```mkdir -p /media/nfs``` <br>
```mount -t nfs 192.168.21.200:/media/partage /media/nfs``` <br>

Vérifier le montage
```df -h``` <br>

Côté client
```apt install nfs-common``` <br>


## 5. Configuration

Démarrage des services NFS
```sudo /etc/init.d/rpcbind start``` <br>
```sudo /etc/init.d/nfs-kernel-server start``` <br>

Vérification
```sudo rpcinfo –p``` <br>

Trouver la service NFS
```sudo rpcinfo –p | grep nfs``` <br>

Partage dans une seule machine
```/media/partage           192.168.21.200(rw,sync,no_root_squash)``` <br>

Partage à plusieur machine
```/media/partage           192.168.21.0/24(rw,sync,no_root_squash)``` <br>

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