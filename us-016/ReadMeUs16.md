# **Objectifs de la Story :**

>En tant qu'administrateur système, 
je veux que tous les membres du groupe projet_linux puissent créer des fichiers dans un dossier donné, mais qu'un utilisateur ne puisse pas supprimer le fichier d'un autre utilisateur (sticky bit) 
afin de partager des données de manière sécurisée.

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


>  Le sticky bit empêche les utilisateurs de supprimer les fichiers dont ils ne sont pas propriétaires, même dans un dossier partagé en écriture dans un groupe  ,la commande est : "sudo chmod +t chemin_dossier",

>[voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-22 154545.png>)

>"drwxrws--T 2 root projet_linux 4096 21 janv. 16:00 /opt/partage"
ici le T represente le sticky bit

>[test](<../us-001/pictures/Capture d'écran 2026-01-23 012939.png>) , ici pour le test , j ai vérifier si le stickybit fonctionne puis j ai créer un fichier qui s appelle fichier_alice.txt avec le user lain , ensuite j ai changé de user de lain a arice , et quand j ai essayer de supprimer le fichier que lain a créer , ce message est apparu "rm: impossible de supprimer 'fichier_alice.txt': Opération non permise"
car ce n est pas arice qui a créer le fichier,
