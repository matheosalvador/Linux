# **Objectifs de la Story :**

>En tant qu'utilisateur, 
je veux surveiller les processus en cours (ps, top), 
afin d’identifier ceux qui consomment le plus de ressources.

# **Critères d'acceptation :**

>Identifier les colonnes clés : PID, %CPU, %MEM, et COMMAND.
>
>Interpréter la charge système sur 1, 5 et 15 minutes pour savoir si le serveur est surchargé.
>
>Trier les processus par consommation de mémoire et par CPU.
>
>Filtrer l'affichage pour ne voir que les processus d'un utilisateur spécifique.
>
>Obtenir une liste complète des processus.
>
>Trouver un processus précis (ps et grep).
>
>Envoyer un signal de terminaison propre ou forcé en comprenant le risque de ce dernier.
>
>Expliquer pourquoi certains processus nécessitent sudo pour être stoppés.