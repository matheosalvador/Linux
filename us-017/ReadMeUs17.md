# **Objectifs de la Story :**

>En tant qu'administrateur système, 
je veux que tous les membres d'un groupe puisse créer un fichier à l'intérieur d'un dossier et que ce fichier appartienne au groupe (sgid) 
afin de partager des données entre membres d'un même groupe.

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

> ici dans la commande pour accorder les permissions on ajoute le "2" : 
"sudo    chmod 2770 /opt/partage";
ici 2 → setgid (héritage du groupe)
>
>Sans setgid, le groupe du fichier est le groupe principal de l’utilisateur.
>
>Avec setgid, le groupe du fichier est celui du dossier, donc Le setgid garantit que  tous les fichiers créés dans un dossier appartiennent automatiquement au même groupe .
![voir sur console ](<../us-001/pictures/Capture d'écran 2026-01-22 160110.png>),
>
>ici dans la  réponse de la commande "sudo    chmod 2770 /opt/partage" qui est "drwxrws--- 2 root projet_linux 4096 21 janv. 16:00 /opt/partage",
 on voit bien le s qui represente le setgid
>
> ![test](<../us-001/pictures/Capture d'écran 2026-01-23 005715.png>) , pour le test sur cette photo ,on a pris le user lain qui fait partie du group projet_linux et on a créer un fichier qui s appelle test_alice.txt , puis on a fait la commande "ls -l pour voir quelle groupe ce fichier a hériter lors de la création , et ici grâce au setgid 
on voit bien que le groupe hérité est le projet_linux,
"-rw-r--r-- 1 lain projet_linux 0 23 janv. 00:56 test_alice.txt" 