# **Objectifs de la Story :**

>En tant que développeur, 
je veux créer un script interactif qui demande à l'utilisateur quel logiciel il souhaite installer (par exemple Git), vérifie s'il est déjà présent, et l'installe si nécessaire.

# **Critères d'acceptation :**

>Tous les scripts commencent par la shebang
>
>Le script d'installation utilise une commande de test pour vérifier la présence du logiciel avant de l'installer.
>
>Le script d'installation gère l'élévation de privilèges ou avertit l'utilisateur qu'il doit être sudo.
>
>Le script de création peut être lancé plusieurs fois sans générer d'erreurs si les dossiers existent déjà.
>
>Les dossiers projets/, docs/ et clones/ sont créés avec les permissions appropriées.
>
>Le script crée l'arborescence dans le répertoire personnel ($HOME) de l'utilisateur qui l'exécute.
>
>Au moins deux alias pointant vers les scripts des US précédentes.
>
>Les modifications sont inscrites dans le fichier ~/.bashrc et restent actives après une déconnexion/reconnexion.
>
>L'invite de commande affiche l'heure actuelle.

# **Résultat :**

>### **Création du script intéractif :**
>
>Créer le ficher avec la commande suivante : **"nano app.nano(install.sh)"**
>
>Mettre le code suivant dans le fichier : 
```bash
"#!/bin/bash

# Vérification que le script est lancé en root
# $EUID : ID de l’utilisateur qui exécute le script
# 0 c est le root
if [ "$EUID" -ne 0 ]; then
        echo "Ce script doit être exécuter en tant que root"
        exit 1
else

clear
echo "=========================================="
echo "     INSTALLATEUR DE LOGICIELS LINUX"
echo "=========================================="
echo ""
echo "Choisissez une application à installer :"
echo ""

echo "  1) Git"
echo "  2) Curl"
echo "  3) Wget"
echo "  4) Htop"
echo "  5) Neofetch"
echo "  6) Unzip / Zip"
echo "  7) build-essential"

echo "  8) Python3 + pip"
echo "  9) NodeJS + npm"
echo " 10) OpenJDK 17"
echo " 11) Docker"
echo " 12) Docker Compose"
echo " 13) GCC / G++"

echo " 14) Apache2"
echo " 15) Nginx"
echo " 16) PHP + modules"
echo " 17) MySQL Server"
echo " 18) MariaDB Server"
echo " 19) Composer"
echo " 20) phpMyAdmin"

echo " 21) Git LFS"
echo " 22) GIMP"
echo " 23) Inkscape"
echo " 24) Blender"
echo " 25) FFmpeg"

echo " 26) Nmap"
echo " 27) Net-tools"
echo " 28) UFW (pare-feu)"
echo " 29) OpenSSH Server"

echo " 30) Vim"
echo " 31) Nano"
echo " 32) Tmux"
echo " 33) Gnome Tweaks"
echo " 34) VLC"

echo " 35) Quitter"
echo ""
read -p "Votre choix : " choix

case $choix in
    1) sudo apt install -y git ;
    2) sudo apt install -y curl ;
    3) sudo apt install -y wget ;
    4) sudo apt install -y htop ;
    5) sudo apt install -y neofetch ;
    6) sudo apt install -y unzip zip ;
    7) sudo apt install -y build-essential ;

    8) sudo apt install -y python3 python3-pip ;
    9) sudo apt install -y nodejs npm ;
   10) sudo apt install -y openjdk-17-jdk ;
   11) sudo apt install -y docker.io ;
   12) sudo apt install -y docker-compose ;
   13) sudo apt install -y gcc g++ ;

   14) sudo apt install -y apache2 ;
   15) sudo apt install -y nginx ;
   16) sudo apt install -y php php-cli php-mysql ;
   17) sudo apt install -y mysql-server ;
   18) sudo apt install -y mariadb-server ;
   19) sudo apt install -y composer ;
   20) sudo apt install -y phpmyadmin ;

   21) sudo apt install -y git-lfs ;
   22) sudo apt install -y gimp ;
   23) sudo apt install -y inkscape ;
   24) sudo apt install -y blender ;
   25) sudo apt install -y ffmpeg ;

   26) sudo apt install -y nmap ;
   27) sudo apt install -y net-tools ;
   28) sudo apt install -y ufw ;
   29) sudo apt install -y openssh-server ;

   30) sudo apt install -y vim ;
   31) sudo apt install -y nano ;
   32) sudo apt install -y tmux ;
   33) sudo apt install -y gnome-tweaks ;
   34) sudo apt install -y vlc ;

   35) echo "Fermeture."; exit 0 ;
    *) echo "Choix invalide." ;
esac

echo "Installation terminée."
fi
```

>Donner les permission d'éxécution au fichier install.sh avec la >commande suivante : **"chmod 775 app.name (install.sh)"**
>
>Puis le lancer avec soit **"sudo bash install.sh"** ou **"sudo ./install.sh"**
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-22 143235.png>)**
>
>Mettre le numéro de son choix et il installe le logiciels demandé
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-22 143301.png>)**
>
>Quitte si le numéro est 35.
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-22 143316.png>)**
>
>Si il est lancer sans sudo il affiche ceci 
>
>**![Voir Exemple](<../us-001/pictures/Capture d'écran 2026-01-22 143215.png>)**
