# **Objectifs de la Story :**

>En tant que responsable d'équipe, 
je veux créer un dossier /opt/partage où tous les membres du groupe peuvent lire et écrire des fichiers, 
mais où les autres n'y ont aucun accès.

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

> d abord créer le le dossier avec "mkdir /opt/partage"
>
> ensuite  le assosier au  groupe voulu : "sudo chown : projet_linux /opt/partage";
>
> puis - Donner les permissions dans le  groupe :     "sudo  chmod 2770 /opt/partage";

    2 → setgid (héritage du groupe)

    7 → propriétaire (root) : rwx

    7 → groupe (projet_linux) : rwx

    0 → autres :  aucun accès

    "drwxrws--- 2 root projet_linux 4096 21 janv. 16:00 /opt/partage" explication : 

    d	dossier
    rwx	root : accès total
    rws	groupe : accès + setgid
    ---	autres : aucun accès
    root	propriétaire
    projet_linux	groupe
    le 2 represente le nombre de lien ici c est le parent .. et le dossier lui même .,
>
>![voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-22 015201.png>)
>
>![test](<../us-001/pictures/Capture d'écran 2026-01-23 015206.png>) , dans ce test , j ai créer un fichier texte avec un user(lain) qui appartient au groupe projet_linux , donc on voit bien que les users qui appartiennent aux groupe peuvent bien écrire des fichiers.
>
>![test](<../us-001/pictures/Capture d'écran 2026-01-23 020210.png>) , dans ce test le user mila qui n est pas root et qu il ne fais pas partie du groupe projet_linux tente d acceder au dossier /opt/partage, sauf que la permission ne lui a pas été accorder car nous avons bloquer tout accés au users qui ne ne font pas partie du groupe projet_linux,
