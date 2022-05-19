## 1. Introduction
C’ est quoi la commande IPTABLE?
Iptables est une interface en ligne de commande permettant de configurer Netfilter. En plus de Iptables, depuis la version 8.04, Ubuntu est installé avec la surcouche UFW qui permet de contrôler simplement Netfilter, UFW est toutefois moins complet que iptables.
Pourquoi utiliser iptables ?
Le pare-feu Iptables Linux est utilisé pour surveiller le trafic entrant et sortant vers un serveur et le filtrer en fonction des règles définies par l'utilisateur, afin d'empêcher toute personne d'accéder au système.

## 2. Installation
apt install iptables

## 3. Type de table
Les table avec les paramètres  par défaut
- Filter : L'emplacement prévu pour ajouter des filtres sur les paquets entrant, sortant et traversant. (INPUT/ OUTPUT/ FORWARD)
- NAT:Permet de faire la traduction d'adresse réseau (NAT) sur différents paquets. (PREROUTING/ POSTROUTING/ OUTPUT)
- MANGLE: Permet de modifier des paquets en changeant les champs de TOS (type de service), et d'autres (PREROUTING/ OUTPUT)

## 4. Options
Accepter le trafic
-j accept

Refuser le trafic
-j drop

