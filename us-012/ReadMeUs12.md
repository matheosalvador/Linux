# **Objectifs de la Story :**

>En tant qu'administrateur système, 
je veux créer des utilisateurs (adduser) appartenant à un
groupe commun nommé projet_linux.

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

>  la commande pour créer un utilisateur est   : "sudo useradd -m username";


> créer le mot de passe du nouveau user : "sudo passwd username";
![voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-21 151730.png>)

> la commande pour vérifier si les users ont bien été créer : " cat /etc/passwd ";
![voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-22 140424.png>)

> la  commande pour créer un groupe est : "sudo groupadd group_name";
![voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-22 141011.png>)


> la commande pour ajouter les users a un group:
 "sudo usermod -a -G groupname username"
ici, “-a” veut dire append, and “-G” specifie le group lequelle le user doit être ajouter ;

> afficher les membres de un groupe :  "getent group nom_group";
![voir sur console](<../us-001/pictures/Capture d'écran 2026-01-22 141521.png>)

