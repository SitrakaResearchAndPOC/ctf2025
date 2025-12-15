# Deroulement : 
## 15/06/2025: 
Information sur les outils à installer
## 16/06/2025 : 
Installation pour chaque groupe des outils (  exegol , docker, vokoscreen ou obs avec format minimal)
## 17/07/2025 :
* AM : Exploration en white box : Les participants auront accés aux machines vulnérables . Tous obligatoires avec docker
* PM : CTF prolab att4ck def3nd  en black blox : Les participants n'auront pas accés aux machines vulnérables. </br>
Les participants penetrent des machines pour pentest et essaie en même temps de protéger contre les autres participants </br>
RQ  : LES PARTICIPANTS DEVRONT FAIRE UNE CAPTURE VIDEO (AVEC LE MOINS DE FRAME ET QUALITE MOYENNE) SUR VOKOSCREEN OU OBS STUDIO. </br>
RQ2 : VEUILLEZ FAIRE DU SAUVEGARDE TOUS LES 30 MINUTES POUR NE PAS ALLOURDIR LA TAILLE DU VIDEO

# 18/07/2025 : Rédaction de rapport  en word et des presentation de 5minutes en excel
* WORD : Montre tous les vulnérabilités exploitées et les impacts des vulnérabilités (des captures d'écran issues des vidéos capturés le 17/12/2025)
* PPT : Montre les vulnérabilités critiques et interessantes à connaitre pour des publiques

# 19/07/2025 :
* Tous les fichiers word et ppt seront déposés avant la présentation du 19/07/20 avant 06H00
* Presentation du PPT (la présentation est sans démos mais les participants peuvent montrés un extrait de vidéo s'ils veulent)
* RQ : La presentation ne doit pas dépassé de 5min

# ctf2025
# CHOIX DE OS : 
* linux avec docker 
* windows : utilisation machine virtuelle (vmware ou virtualbox) avec une machine linux (lubuntu ou xubuntu qui ne depense pas trop mémoire RAM)
Les outils vmware et lubuntu/xubuntu et d autres logiciels seront déposé dans le serveur local de l'INSI à partir de 16/12/2025 pour ne pas télécharger l'image exegol plus de 45giga 


# INSTALLATION EXEGOL
* Exegol : un outil de pentester se basant sur une surcouche (wrapper) python de docker.

# ETAPE 1 : LIRE LA DOCUMENTATION
[documentation](https://docs.exegol.com)
[document1](https://www.youtube.com/watch?v=RxGkG8HFFHs&t=570s)
[document2](https://www.youtube.com/watch?v=2tWBn86R-o4)
[document3](https://www.youtube.com/watch?v=hg4kUPXUt7g&t=14s)
[document4](https://www.youtube.com/watch?v=8PptL7FDJcY)
[document5](https://www.youtube.com/watch?v=PYPcpDGELqM)
[document6](https://www.youtube.com/watch?v=E8TAZ_J_H8s)
[document7](https://www.youtube.com/watch?v=XwmbUA-k38E&pp=0gcJCSUKAYcqIYzv)
[document8](https://www.youtube.com/watch?v=-U-vP_RmAZk&t=9s)
[document9](https://www.youtube.com/watch?v=EMhUooNQE3I)
[document10](https://www.youtube.com/watch?v=o9G4Q-2sI4s)
[document11](https://www.youtube.com/watch?v=-U-vP_RmAZk)
[document12](https://www.youtube.com/watch?v=mrRNabBL9eE)
[document13](https://www.youtube.com/watch?v=KBaek8qJPMs)
[document14](https://www.youtube.com/watch?v=wpwKky8lOAI)
[document15](https://www.youtube.com/watch?v=ltgpmOynCc4)

RQ : CHERCHE LE FICHIER EXCEL QUI LISTE TOUS LES OUTILS POSSIBLES

# ETAPE 2 : INSTALLATION DES DEPENDANCES
```
apt update
```
```
apt install vokoscreen
```
```
apt install docker.io
```
```
apt install pipx
```
```
pipx ensurepath
```
```
pipx install exegol
```
```
pipx upgrade exegol
```
>> redemarrer le PC 

# ETAPE 3 : CHARGEMENT D'IMAGES
L’image full est payante par défaut sauf si l'image est préfabriquée. </br>
</br>
* Beacoup des versions d'image d'exegol existe mais pour ce qui sera partagé dans le serveur local est : LAST DU 04_12_2025
* D'autres anciennes images de NWODTUHS peuvent utilisées pour le concours CTF mais ne sera pas déposé dans le serveur : [docker_nwodtuhs](https://hub.docker.com/r/nwodtuhs/exegol)
Selon les domaines de cybersecurité, les images peuvent être :
* FREE
* FULL
* OSINT
* AD
* LIGHT
* WEB
* RQ : N'UTILISER PAS LA VERSION FREE QUI POSSEDE PEUT D'OUTILS
 
* ETAPE 4 : COMMANDE POUR CHARGER L'IMAGE
Telecharger l'image : 
```
docker load -i  nwodtuhs_exegol_full_04_12_2025.tar.gz
```
```
docker images
```
* ETAPE 5 : TESTER EXEGOL
```
exegol info
```
master ici sera le nom du conteneur 
```
exegol  start master full-04-12-2025
```
Les commandes exegol sont très proches de docker et travaillent avec docker (surcouche de docker pour faciliter les paramètres courants utilisés dans le ctf dès qu'on connait le nom de commande).
RQ : Dans le workspace master : 
* UTILISER LES TOUCHES DE DIRECTIONS HAUT ET BAS UNE FOIS TAPEE LE COMMANDE COMME NMAP PAR EXEMPLE
* UTILISER LA TOUCHE DROITE POUR VALIDER LE CHOIX DE COMMANDE , IL EST POSSIBLE AUSSI D'UTILISER EXPORT POUR LES PARAMETRES
Dans un autre terminal : Tapez ctrl+shift+T
```
docker ps
```
* ETAPE 5 : REALISATION DE DEMO FILE UPLOAD AVEC DVWA
Un démo sera déposé au serveur INSI à partir de 16/12/2025
[document1](https://www.youtube.com/watch?v=RxGkG8HFFHs&t=570s)
