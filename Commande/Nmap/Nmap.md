[Go to Readme.md](https://github.com/Ezdev2/Sys1-exam/blob/339c2029e1b0f42828993adb922f40f8ca4defb9/README.md)

***

## 1. Description
Nmap, abréviation de Network Mapper, est un outil gratuit et open source pour l'analyse des vulnérabilités et la découverte de réseaux. Les administrateurs réseau utilisent Nmap pour identifier les périphériques exécutés sur leurs systèmes, découvrir les hôtes disponibles et les services qu'ils proposent, rechercher les ports ouverts et détecter les risques de sécurité.

## 2. Syntaxe
```nmap {cible(s)} ```<br>
exemple : ```nmap 192.168.1.1```<br>

```nmap [type du scan] [option] {spécifications des cibles}```<br>

Type du scan:
- ```-sP``` : équivalent à ping, pour voir si le cible est active (alive) 
exemple: # nmap -sp 192.100.1.1/24
- ```-sV```: Teste les ports ouverts pour déterminer le service en écoute, et sa version
- ```-sS``` : scan des ports TCP, envoie d’un message SYN pour l’ouverture d’une connexion TCP puis attente de la réponse.

Les options
- ```-oG``` : sortie output grepable
- ```-T4``` : l’agressivité (pour scanner plus ou moins vite) 
- ```-A``` : détection de la version et OS

Spécification du cible
network : ```www.google.com``` <br>
ip address : ```192.xxx.xx.xx``` <br>
hostname: ```nom d’hôte``` <br>

## 3. Installation
```sudo apt-get update ``` <br>
(Sert pour mettre à jour la liste des fichiers disponibles dans les dépôts APT qu’on peut trouvé dans le fichier de configuration /etc/apt/sources.list)

```sudo apt-get install nmap ``` <br>
(Installer nmap)

## 4. Généralités
Nmap permet de récupérer simplement une liste de ports ouverts sur une machine, de découvrir toutes les machines d’un réseau, mais aussi de savoir quel système d’exploitation elles utilisent.

Les exemples qu’on va voir:
commande nmap pour: 
- Récupérer la liste de ports ouverts
- Voir l’état des ports spécifiques 
- Vérifier le système d’exploitation

## 5. Liste des commandes Nmap et leur rôles (certaines commandes)

1- Scanner un seul host :
```# nmap 192.168.1.1``` <br>
```# nmap www.exemple.com``` <br>

2- Scanner plusieurs adresse IP :
```# nmap 192.168.16.6 192.168.16.2 192.168.16.8``` <br>

3- scanner une plage d’adresses :
```# nmap 192.168.10,.0-255 (Cette commande scanne les adresses de 192.168.10.0 à 192.168.10.255)``` <br>

4-Scanner une plage d’adresse en utilisant le Wildcard :
```# nmap 192.168.1.*``` <br>

5-Scanner un sous-réseau :
```# nmap 192.168.1.0/``` <br>

6- Scan de ports ouverts :
```# nmap -sS 192.168.1.3``` <br>

7- Détecter le système d’exploitation d’une machine :
```# nmap -O 192.168.1.3nmap -v -O --osscan-guess 192.168.1.1``` <br>

8- Le scan rapide rechercher les ports répertoriés dans les fichiers nmap-services, cela permet de recenser les principaux services réseaux.
Pour cela, on utilise l’option ```-F de Nmap :``` <br>
```nmap -F 192.168.1.1``` <br>

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