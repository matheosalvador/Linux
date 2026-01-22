# **Objectifs de la Story :**

>En tant que développeur, 
je veux créer un script pour automatiser la création d'utilisateurs et leur suppression afin de gagner du temps lors de configurations répétées.

# **Critères d'acceptation :**

>Aucune action n'est effectuée directement avec root (sudo).
>
>Existence d'au moins trois utilisateurs tests dans le groupe.
>
>Un script permet de créer un utilisateur.
>
>Le script ne plante pas si l'utilisateur à créer existe déjà.
>
>Un script permet de supprimer proprement un utilisateur.
>
>Le script effectue le nettoyage du répertoire /home de l'utilisateur.
>
>Le script ne plante pas si l'utilisateur à supprimer n'existe pas.
>
>Le répertoire /opt/partage appartient à root pour le propriétaire et à projet_linux pour le groupe.
>
>Les droits interdisent tout accès aux utilisateurs n'appartenant pas au groupe.
>
>Tout nouveau fichier créé à l'intérieur hérite automatiquement du groupe projet_linux.
>
>Un membre du groupe peut modifier ses fichiers mais ne peut pas supprimer ceux des autres membres.
>
>Les permissions de /etc/shadow sont vérifiées : seul root peut y accéder.


# **Resultat:**

> ici pour créer un script , on fait: " nano nom_fichier" puis  en ajoute dans le script 
#!/bin/bash pour que l interpréteur soit bash par défaut,
> voici le script pour  automatiser la création d'utilisateurs et leur suppression:
[voir la console](<../us-001/pictures/Capture d'écran 2026-01-22 152255.png>) ,

> exemple de utilisation:
[voir sur console](<../us-001/pictures/Capture d'écran 2026-01-22 152708.png>) ,

> ici on voit bien que le utilisateur "miao" a bien été ajouter : [voir sur console](<../us-001/pictures/Capture d'écran 2026-01-22 152956.png>) ,

> ici on gére bien les erreurs:
[voir sur console](<../us-001/pictures/Capture d'écran 2026-01-22 153556.png>)

