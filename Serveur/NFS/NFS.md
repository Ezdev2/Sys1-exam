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
apt-get nfs-kernel-server
apt install nfs-kernel-server(se référer sur les vidéo semaine 5 sur l’installation des packages)

Créer le dossier et/ou fichierà paartager dans:
/etc/exports

Créer un repertoire
mkdir -p /media/nfs
mount -t nfs 192.168.21.200:/media/partage /media/nfs

Vérifier le montage
df -h

Côté client
apt install nfs-common


## 5. Configuration

Démarrage des services NFS
sudo /etc/init.d/rpcbind start
sudo /etc/init.d/nfs-kernel-server start

Vérification
sudo rpcinfo –p

Trouver la service NFS
sudo rpcinfo –p | grep nfs

Partage dans une seule machine
/media/partage           192.168.21.200(rw,sync,no_root_squash)

Partage à plusieur machine
/media/partage           192.168.21.0/24(rw,sync,no_root_squash)