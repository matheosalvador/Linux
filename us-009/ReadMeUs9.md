# instructions pour l'utilisateur

>Utiliser les commandes `ps` et `top` pour lister les processus en cours :
>
>- [Commande PS.](../us-001/pictures/PSCMD.png)
>
>- [Commande TOP.](../us-001/pictures/TOPCMD.png) 
>
>Colonnes importantes à comprendre dans la sortie des commandes :
>
>- PID : Identifiant du processus. (1ere colonne)
>- %CPU : Pourcentage de l'utilisation du CPU par le processus. (7eme colonne)
>- %MEM : Pourcentage de l'utilisation de la mémoire par le processus. (8eme colonne)
>
>Load Average : Indique la charge moyenne du système sur 1, 5 et 15 minutes :
>
>- [UPDATE Commande](../us-001/pictures/LoadAverage.png)
>
>Trier les processus par consommation CPU puis Memoire :
>
>- [Tri par CPU](../us-001/pictures/%CPU.png) 
>- [Tri par MEM](../us-001/pictures/%MEM.png) 
>
>Filtrer l'affichage pour ne voir que les processus d'un utilisateur spécifique.
>
>[Filtre Utilisateur](../us-001/pictures/FiltreBobby.png)
>
>Liste complète du processsus :
>
>- [Liste Complete](../us-001/pictures/CompleteProc.png)
>
>Trouver un processus précis :
>
>- [Processus precis](../us-001/pictures/SpecProc.png)
Envoyer un signal de terminaison propre ou forcé :
>
>SIGTERM = Signal de terminaison propre.
>
>- [SIGTERM commande](../us-001/pictures/SIGTERM.png)
>
>SIGKILL = Signal de terminaison forcée.
>
>- [SIGKILL commande](../us-001/pictures/SIGKILL.png)
>
>Il faut utiliser sudo parce que ces processus appartiennent au système (root), donc il faut les droits d'admin pour pouvoir les stopper sans que Linux nous bloque.