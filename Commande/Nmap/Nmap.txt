1. Description
Nmap, abréviation de Network Mapper, est un outil gratuit et open source pour l'analyse des vulnérabilités et la découverte de réseaux. Les administrateurs réseau utilisent Nmap pour identifier les périphériques exécutés sur leurs systèmes, découvrir les hôtes disponibles et les services qu'ils proposent, rechercher les ports ouverts et détecter les risques de sécurité.

2. Syntaxe
nmap {cible(s)} 
exemple : nmap 192.168.1.1

nmap [type du scan] [option] {spécifications des cibles}

Type du scan:
- sP : équivalent à ping, pour voir si le cible est active (alive) 
exemple: # nmap -sp 192.100.1.1/24
-sV: Teste les ports ouverts pour déterminer le service en écoute, et sa version
-sS : scan des ports TCP, envoie d’un message SYN pour l’ouverture d’une connexion TCP puis attente de la réponse.

Les options
-oG : sortie output grepable
-T4 : l’agressivité (pour scanner plus ou moins vite) 
-A : détection de la version et OS

Spécification du cible
network : www.google.com
ip address : 192.xxx.xx.xx
hostname: nom d’hôte

3. Installation
sudo apt-get update 
(Sert pour mettre à jour la liste des fichiers disponibles dans les dépôts APT qu’on peut trouvé dans le fichier de configuration /etc/apt/sources.list)

sudo apt-get install nmap 
(Installer nmap)

4. Généralités
Nmap permet de récupérer simplement une liste de ports ouverts sur une machine, de découvrir toutes les machines d’un réseau, mais aussi de savoir quel système d’exploitation elles utilisent.

Les exemples qu’on va voir:
commande nmap pour: 
- Récupérer la liste de ports ouverts
- Voir l’état des ports spécifiques 
- Vérifier le système d’exploitation

5. Liste des commandes Nmap et leur rôles (certaines commandes)
1- Scanner un seul host :
#nmap 192.168.1.1
#nmap www.exemple.com

2- Scanner plusieurs adresse IP :
#nmap 192.168.16.6 192.168.16.2 192.168.16.8

3- scanner une plage d’adresses :
#nmap 192.168.10,.0-255 (Cette commande scanne les adresses de 192.168.10.0 à 192.168.10.255)

4-Scanner une plage d’adresse en utilisant le Wildcard :
#nmap 192.168.1.*

5-Scanner un sous-réseau :
#nmap 192.168.1.0/24

6- Scan de ports ouverts :
#nmap -sS 192.168.1.3

7- Détecter le système d’exploitation d’une machine :
#nmap -O 192.168.1.3nmap -v -O --osscan-guess 192.168.1.1

8- Le scan rapide rechercher les ports répertoriés dans les fichiers nmap-services, cela permet de recenser les principaux services réseaux.
Pour cela, on utilise l’option -F de Nmap :

nmap -F 192.168.1.1

