# **Objectifs de la Story :**

En tant qu’utilisateur, 
je veux naviguer dans l’arborescence Linux avec des commandes de base
afin de me familiariser avec le système.

# **Critères d'acceptation :**

Identifier son emplacement actuel dans l'arborescence de dossiers.

Faire la différence entre un chemin absolu et un chemin relatif.

Revenir instantanément à son dossier personnel.

Se déplacer dans le dossier parent.

Lister les fichiers, cachés ou non.

Se rendre dans les dossiers clés et d'expliquer brièvement leur rôle comme /etc , /var/log et /home

Utiliser l'auto-complétion avec la touche Tab pour éviter les erreurs de frappe.

Utiliser l'historique de commandes afin d'exécuter à nouveau une commande.



# **Resultat :** 

> - pour Identifier son emplacement actuel dans l'arborescence de dossiers la commande est : "pwd";

> - le chemin absolu indique l’emplacement exact et complet d’un fichier ou dossier depuis la racine du système.il commence par / sur linux

> exemple : /home/selmen/Documents/cours/java.txt
Peu importe où je me trouve, ce chemin pointe toujours vers le même fichier.

> - le chemin relatif indique l’emplacement par rapport au dossier où je suis  actuellement.Il dépend du répertoire ou je suis ,
.. = reculer d’un dossier
>exemple: ../java.txt



> exemple : si je suis dans /home/selmen/Documents
et que je écris cours/java.txt  le systeme comprend
/home/selmen/Documents/cours/java.txt

> - pour Revenir instantanément à son dossier personnel
la commande est : "cd"

> - Se déplacer dans le dossier parent la  commande est :"cd .."

> - Lister les fichiers, cachés ou non. la commande est 
"ls -la"



> - le role de /etc est de Contenir  les fichiers de configuration du système
Paramètres des services (réseau, utilisateurs, sudo, etc.)
Exemple :
/etc/hostname → nom de la machine
/etc/passwd → infos sur les utilisateurs
S’y rendre : cd /etc/
[voir exemple sur console ](<../us-001/pictures/Capture d'écran 2026-01-21 113701.png>)

> - le role de /var/log est  de Contenir  les journaux du système,
Sert à comprendre les erreurs et événements.
Exemple :
syslog → événements généraux
auth.log → connexions, sudo, sécurité
S'y rendre : cd /var/log
[voir exemple sur console ](../us-001/pictures/image.png)

> - le role de /home  est de Contenir les dossiers personnels des utilisateurs,
Chaque utilisateur a son espace
Exemple :
/home/selmen
S'y rendre: cd /home
[voir exemple sur console ](<../us-001/pictures/Capture d'écran 2026-01-21 120001.png>)

> - Utiliser l'auto-complétion avec la touche Tab pour éviter les erreurs de frappe.PRATIQUE

> - Utiliser l'historique de commandes afin d'exécuter à nouveau une commande. la commande est :"history"
Réexécuter une commande avec son numéro : !puis le numéro de la commande 
[voir exemple sur console pour le history ](<../us-001/pictures/Capture d'écran 2026-01-21 122057.png>)-
[voir exemple sur console pour la réexécution de commande via history ](<../us-001/pictures/Capture d'écran 2026-01-21 122327.png>)
par exemple aprés avoir fait la commande "history" et aprés avoir eu la liste des commandes , si je veux 
relancer la commande "pwd" qui est au numéro 140 ,je fais
!140.



