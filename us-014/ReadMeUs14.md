# **Objectifs de la Story :**

>En tant qu'auditeur, 
je veux utiliser les commandes chown et chmod pour m'assurer que les informations sensibles comme /etc/shadow ou /opt/partage sont bien protégées et illisibles par un nouvel utilisateur.

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

> pour changer les permissions d’un dossier (ou d’un fichier), on utilise:
  "sudo chmod permissions chemin_du_dossier"

>du coup ici je fais "sudo chmod 600 /etc/shadow"
[voir sur console](<../us-001/pictures/Capture d'écran 2026-01-22 145135.png>) ,
ici j ai accordé les permissions de read and write seulement a root    ,personne d autres a accés au fichier  /etc/shadow ,
[voir sur console](<../us-001/pictures/Capture d'écran 2026-01-22 1433010.png>)

> on utilise le même principe pour /opt/partage avec 
 la commande "sudo chmod 2770 /opt/partage"
[voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-22 150127.png>),
  "drwxrws--- 2 root projet_linux 4096 21 janv. 16:00 /opt/partage",
 ici le "---" 
 indique bien que les users qui ne font pas partie du groupe projet_linux peuvent ni read ou write et ni exécuter.

 >[test](<../us-001/pictures/Capture d'écran 2026-01-23 014034.png>) , dans le test je tente de read le fichier ,
 sauf que comme on a indiquer avec les commandes en haut que seul root doit avoir les droits de read and write  â ce fichier ,donc arice  n 'a pas la permission de read le fichier même si le user fais  partie du groupe projet_linux, car le user est pas root.








