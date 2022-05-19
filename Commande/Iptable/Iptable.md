[Go to Readme.md](https://github.com/Ezdev2/Sys1-exam/blob/339c2029e1b0f42828993adb922f40f8ca4defb9/README.md)

***

## 1. Introduction
C’ est quoi la commande IPTABLE?
Iptables est une interface en ligne de commande permettant de configurer Netfilter. En plus de Iptables, depuis la version 8.04, Ubuntu est installé avec la surcouche UFW qui permet de contrôler simplement Netfilter, UFW est toutefois moins complet que iptables.
Pourquoi utiliser iptables ?
Le pare-feu Iptables Linux est utilisé pour surveiller le trafic entrant et sortant vers un serveur et le filtrer en fonction des règles définies par l'utilisateur, afin d'empêcher toute personne d'accéder au système.

## 2. Installation
```apt install iptables``` <br>

## 3. Type de table
Les table avec les paramètres  par défaut
- Filter : L'emplacement prévu pour ajouter des filtres sur les paquets entrant, sortant et traversant. ```INPUT/ OUTPUT/ FORWARD``` <br>
- NAT:Permet de faire la traduction d'adresse réseau (NAT) sur différents paquets. ```PREROUTING/ POSTROUTING/ OUTPUT``` <br>
- MANGLE: Permet de modifier des paquets en changeant les champs de TOS (type de service), et d'autres ```PREROUTING/ OUTPUT``` <br>

## 4. Options
Accepter le trafic
```-j accept``` <br>

Refuser le trafic
```-j drop``` <br>

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